---
title: Messaggio FILEOKSTRING (Commdlg.h)
description: Una finestra di dialogo Apri o Salva con nome invia il messaggio registrato fileOKSTRING alla procedura hook OFNHookProc, quando l'utente specifica un nome di file e fa clic sul pulsante OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Finestre di dialogo del messaggio FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24dd07faecc66bc50c408eab36bcbd8c93c460ef
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549216"
---
# <a name="fileokstring-message"></a><span data-ttu-id="2682a-104">Messaggio FILEOKSTRING</span><span class="sxs-lookup"><span data-stu-id="2682a-104">FILEOKSTRING message</span></span>

<span data-ttu-id="2682a-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="2682a-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="2682a-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="2682a-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="2682a-107">Una finestra  **di** dialogo Apri o Salva con nome invia il messaggio registrato **fileOKSTRING** alla procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)quando l'utente specifica un nome di file e fa clic sul **pulsante OK.**</span><span class="sxs-lookup"><span data-stu-id="2682a-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="2682a-108">La procedura hook può accettare il nome del file e consentire la chiusura della finestra di dialogo oppure rifiutare il nome del file e forzare la finestra di dialogo a rimanere aperta.</span><span class="sxs-lookup"><span data-stu-id="2682a-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="2682a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2682a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2682a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2682a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2682a-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2682a-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2682a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2682a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2682a-113">Puntatore a una [**struttura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)</span><span class="sxs-lookup"><span data-stu-id="2682a-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="2682a-114">Il **membro lpstrFile** di questa struttura contiene l'unità, il percorso e il nome file specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2682a-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2682a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2682a-115">Return value</span></span>

<span data-ttu-id="2682a-116">Se la routine hook restituisce zero, la **finestra di** dialogo Apri o **Salva** con nome accetta il nome file specificato e viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="2682a-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="2682a-117">Se la routine hook restituisce un  valore  diverso da zero, la finestra di dialogo Apri o Salva con nome rifiuta il nome file specificato e rimane aperta.</span><span class="sxs-lookup"><span data-stu-id="2682a-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="2682a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2682a-118">Remarks</span></span>

<span data-ttu-id="2682a-119">La routine hook deve specificare la **costante FILEOKSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2682a-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2682a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2682a-120">Requirements</span></span>



| <span data-ttu-id="2682a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2682a-121">Requirement</span></span> | <span data-ttu-id="2682a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2682a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2682a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2682a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2682a-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2682a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2682a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2682a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2682a-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2682a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2682a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2682a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2682a-128"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2682a-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2682a-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2682a-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2682a-130">**FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2682a-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="2682a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2682a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2682a-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2682a-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2682a-133">**FILEOK della rete CDN \_**</span><span class="sxs-lookup"><span data-stu-id="2682a-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="2682a-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="2682a-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="2682a-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="2682a-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="2682a-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2682a-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2682a-137">Libreria di finestre di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="2682a-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

