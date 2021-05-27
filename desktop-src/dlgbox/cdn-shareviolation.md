---
title: CDN_SHAREVIOLATION di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse quando l'utente fa clic sul pulsante OK e si verifica una violazione della condivisione di rete per il file selezionato.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION di dialogo del codice di notifica
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
ms.openlocfilehash: 77cd862fa1c3598a4e81a776004f26ef02290477
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548856"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="98222-104">Codice di notifica \_ SHAREVIOLATION della rete CDN</span><span class="sxs-lookup"><span data-stu-id="98222-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="98222-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="98222-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="98222-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="98222-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="98222-107">Inviato da una  finestra  di dialogo Apri o Salva con nome di tipo Esplora risorse quando l'utente fa clic sul pulsante **OK** e si verifica una violazione della condivisione di rete per il file selezionato.</span><span class="sxs-lookup"><span data-stu-id="98222-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="98222-108">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="98222-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="98222-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="98222-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98222-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98222-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98222-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="98222-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98222-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98222-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98222-113">Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="98222-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="98222-114">Il **membro pszFile** di questa struttura è un puntatore al nome del file che ha avuto la violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="98222-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="98222-115">La **struttura OFNOTIFY** contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di codice indica il messaggio di notifica **\_ SHAREVIOLATION** della rete CDN. </span><span class="sxs-lookup"><span data-stu-id="98222-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98222-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98222-116">Return value</span></span>

<span data-ttu-id="98222-117">Il valore restituito indica il modo in cui la finestra di dialogo deve gestire la violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="98222-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="98222-118">Se la routine hook restituisce zero, nella finestra di dialogo viene visualizzato il messaggio di avviso standard per una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="98222-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="98222-119">Per impedire la visualizzazione del messaggio di avviso standard, restituire un valore diverso da zero dalla routine hook e chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare uno dei valori **\_ MSGRESULT DWL** seguenti.</span><span class="sxs-lookup"><span data-stu-id="98222-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="98222-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="98222-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="98222-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98222-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98222-122"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="98222-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="98222-123">Fa in modo che la finestra di dialogo restituirà il nome del file senza avvisare l'utente della violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="98222-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="98222-124"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="98222-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="98222-125">Fa sì che la finestra di dialogo rifiuti il nome del file senza avvisare l'utente della violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="98222-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="98222-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="98222-126">Remarks</span></span>

<span data-ttu-id="98222-127">Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="98222-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="98222-128">Il sistema invia questa notifica solo se il **valore DI \_ SHAREAWARE OFN** non è stato specificato al momento della creazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="98222-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="98222-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98222-129">Requirements</span></span>



| <span data-ttu-id="98222-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="98222-130">Requirement</span></span> | <span data-ttu-id="98222-131">Valore</span><span class="sxs-lookup"><span data-stu-id="98222-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98222-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98222-132">Minimum supported client</span></span><br/> | <span data-ttu-id="98222-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98222-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="98222-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98222-134">Minimum supported server</span></span><br/> | <span data-ttu-id="98222-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98222-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98222-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98222-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="98222-137"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="98222-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98222-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98222-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="98222-139">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="98222-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98222-140">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="98222-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="98222-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="98222-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="98222-142">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="98222-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="98222-143">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="98222-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="98222-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="98222-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="98222-145">**Setwindowlong**</span><span class="sxs-lookup"><span data-stu-id="98222-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="98222-146">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="98222-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98222-147">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="98222-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

