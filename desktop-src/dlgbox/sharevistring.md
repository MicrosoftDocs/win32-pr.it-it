---
title: Messaggio SHAREVISTRING (COMMDLG. h)
description: Una finestra di dialogo Apri o Salva con nome Invia il messaggio SHAREVISTRING registrato alla routine hook, OFNHookProc, se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante OK.
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
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477980"
---
# <a name="sharevistring-message"></a><span data-ttu-id="97202-104">Messaggio SHAREVISTRING</span><span class="sxs-lookup"><span data-stu-id="97202-104">SHAREVISTRING message</span></span>

<span data-ttu-id="97202-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="97202-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="97202-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="97202-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="97202-107">Una finestra di dialogo **Apri** o **Salva con nome** invia il messaggio **SHAREVISTRING** registrato alla routine hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="97202-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="97202-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="97202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97202-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97202-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97202-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="97202-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="97202-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97202-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97202-112">Puntatore a una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="97202-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="97202-113">Il membro **lpstrFile** della struttura contiene il nome del file che ha causato la violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="97202-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97202-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97202-114">Return value</span></span>

<span data-ttu-id="97202-115">La routine hook deve restituire uno dei valori seguenti per indicare la modalità di gestione della violazione di condivisione da parte della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="97202-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="97202-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="97202-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="97202-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97202-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="97202-118"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="97202-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="97202-119">Accetta il nome del file</span><span class="sxs-lookup"><span data-stu-id="97202-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="97202-120"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="97202-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="97202-121">Rifiutare il nome del file ma non avvisare l'utente.</span><span class="sxs-lookup"><span data-stu-id="97202-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="97202-122">L'applicazione è responsabile della visualizzazione di un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="97202-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="97202-123"><dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="97202-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="97202-124">Rifiutare il nome del file e visualizzare un messaggio di avviso, ovvero lo stesso risultato di una procedura di hook.</span><span class="sxs-lookup"><span data-stu-id="97202-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="97202-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="97202-125">Remarks</span></span>

<span data-ttu-id="97202-126">La routine hook deve specificare la costante **SHAREVISTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="97202-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="97202-127">La finestra di dialogo Invia il messaggio **SHAREVISTRING** registrato solo se non è stato specificato il flag **OFN \_ SHAREAWARE** nel membro **Flags** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando è stata creata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="97202-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="97202-128">Se la routine hook restituisce un valore non definito, la finestra di dialogo risponde come se **OFN \_ SHAREWARN** fosse stato restituito.</span><span class="sxs-lookup"><span data-stu-id="97202-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="97202-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97202-129">Requirements</span></span>



| <span data-ttu-id="97202-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="97202-130">Requirement</span></span> | <span data-ttu-id="97202-131">Valore</span><span class="sxs-lookup"><span data-stu-id="97202-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97202-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97202-132">Minimum supported client</span></span><br/> | <span data-ttu-id="97202-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97202-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="97202-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97202-134">Minimum supported server</span></span><br/> | <span data-ttu-id="97202-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97202-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97202-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97202-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="97202-137"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97202-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="97202-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="97202-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="97202-139">**SHAREVISTRINGW** (Unicode) e **SHAREVISTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="97202-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="97202-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97202-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="97202-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="97202-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97202-142">**SHAREVIOLATION rete CDN \_**</span><span class="sxs-lookup"><span data-stu-id="97202-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="97202-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="97202-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="97202-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="97202-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="97202-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="97202-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="97202-146">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="97202-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

