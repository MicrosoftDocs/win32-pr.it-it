---
title: Codice di notifica CDN_SHAREVIOLATION (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando l'utente fa clic sul pulsante OK e si verifica una violazione di condivisione di rete per il file selezionato.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- Finestre di dialogo CDN_SHAREVIOLATION codice di notifica
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acfa3a91e9c84f15984285f99d071fcde24a4d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301590"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="b22f4-104">Codice di notifica SHAREVIOLATION della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="b22f4-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="b22f4-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b22f4-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="b22f4-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="b22f4-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b22f4-107">Inviato da una finestra di dialogo **Apri** o **Salva con nome in** stile esploratore quando l'utente fa clic sul pulsante **OK** e si verifica una violazione di condivisione di rete per il file selezionato.</span><span class="sxs-lookup"><span data-stu-id="b22f4-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="b22f4-108">La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b22f4-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="b22f4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b22f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b22f4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b22f4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b22f4-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="b22f4-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b22f4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b22f4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b22f4-113">Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="b22f4-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="b22f4-114">Il membro **pszFile** di questa struttura è un puntatore al nome del file in cui si è verificata la violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="b22f4-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="b22f4-115">La struttura **OFNOTIFY** contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ SHAREVIOLATION** della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="b22f4-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b22f4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b22f4-116">Return value</span></span>

<span data-ttu-id="b22f4-117">Il valore restituito indica la modalità di gestione della violazione di condivisione da parte della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b22f4-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="b22f4-118">Se la routine hook restituisce zero, nella finestra di dialogo viene visualizzato il messaggio di avviso standard per una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="b22f4-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="b22f4-119">Per evitare la visualizzazione del messaggio di avviso standard, restituire un valore diverso da zero dalla routine hook e chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare uno dei valori **\_ MSGRESULT DWL** seguenti.</span><span class="sxs-lookup"><span data-stu-id="b22f4-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="b22f4-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b22f4-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="b22f4-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b22f4-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b22f4-122"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b22f4-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b22f4-123">Fa in modo che la finestra di dialogo restituisca il nome del file senza avvisare l'utente sulla violazione della condivisione.</span><span class="sxs-lookup"><span data-stu-id="b22f4-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="b22f4-124"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b22f4-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="b22f4-125">Fa in modo che la finestra di dialogo rifiuti il nome del file senza avvisare l'utente sulla violazione della condivisione.</span><span class="sxs-lookup"><span data-stu-id="b22f4-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b22f4-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b22f4-126">Remarks</span></span>

<span data-ttu-id="b22f4-127">Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="b22f4-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="b22f4-128">Questa notifica viene inviata dal sistema solo se il valore **\_ SHAREAWARE di OFN** non è stato specificato al momento della creazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b22f4-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22f4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b22f4-129">Requirements</span></span>



| <span data-ttu-id="b22f4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b22f4-130">Requirement</span></span> | <span data-ttu-id="b22f4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b22f4-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b22f4-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b22f4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b22f4-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b22f4-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b22f4-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b22f4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b22f4-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b22f4-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b22f4-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b22f4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b22f4-137"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b22f4-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b22f4-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b22f4-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="b22f4-139">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b22f4-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b22f4-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b22f4-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b22f4-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="b22f4-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b22f4-142">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="b22f4-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="b22f4-143">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b22f4-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="b22f4-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b22f4-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="b22f4-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="b22f4-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="b22f4-146">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b22f4-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b22f4-147">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="b22f4-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

