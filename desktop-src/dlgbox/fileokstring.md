---
title: Messaggio FILEOKSTRING (COMMDLG. h)
description: Una finestra di dialogo Apri o Salva con nome Invia il messaggio registrato FILEOKSTRING alla routine hook, OFNHookProc, quando l'utente specifica un nome file e fa clic sul pulsante OK.
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
ms.openlocfilehash: 61208ddebc63f1186c2947416e451231f0bea24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478982"
---
# <a name="fileokstring-message"></a><span data-ttu-id="20cbb-104">Messaggio FILEOKSTRING</span><span class="sxs-lookup"><span data-stu-id="20cbb-104">FILEOKSTRING message</span></span>

<span data-ttu-id="20cbb-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="20cbb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="20cbb-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="20cbb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="20cbb-107">Una finestra di dialogo **Apri** o **Salva con** nome Invia il messaggio registrato **FILEOKSTRING** alla routine hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), quando l'utente specifica un nome file e fa clic sul pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="20cbb-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="20cbb-108">La procedura di hook può accettare il nome del file e consentire la chiusura della finestra di dialogo oppure rifiutare il nome del file e forzare la finestra di dialogo in modo che rimanga aperta.</span><span class="sxs-lookup"><span data-stu-id="20cbb-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="20cbb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="20cbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20cbb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20cbb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20cbb-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="20cbb-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20cbb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20cbb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20cbb-113">Puntatore a una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="20cbb-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="20cbb-114">Il membro **lpstrFile** della struttura contiene l'unità, il percorso e il nome file specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="20cbb-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20cbb-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20cbb-115">Return value</span></span>

<span data-ttu-id="20cbb-116">Se la routine hook restituisce zero, la finestra di dialogo **Apri** o **Salva con** nome accetta il nome file specificato e si chiude.</span><span class="sxs-lookup"><span data-stu-id="20cbb-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="20cbb-117">Se la routine hook restituisce un valore diverso da zero, la finestra di dialogo **Apri** o **Salva con** nome rifiuta il nome file specificato e rimane aperto.</span><span class="sxs-lookup"><span data-stu-id="20cbb-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="20cbb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="20cbb-118">Remarks</span></span>

<span data-ttu-id="20cbb-119">La routine hook deve specificare la costante **FILEOKSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="20cbb-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cbb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20cbb-120">Requirements</span></span>



| <span data-ttu-id="20cbb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="20cbb-121">Requirement</span></span> | <span data-ttu-id="20cbb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="20cbb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20cbb-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cbb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="20cbb-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="20cbb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="20cbb-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cbb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="20cbb-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="20cbb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20cbb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20cbb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="20cbb-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20cbb-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="20cbb-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="20cbb-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="20cbb-130">**FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="20cbb-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="20cbb-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20cbb-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="20cbb-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="20cbb-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="20cbb-133">**FILEOK rete CDN \_**</span><span class="sxs-lookup"><span data-stu-id="20cbb-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="20cbb-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="20cbb-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="20cbb-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="20cbb-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="20cbb-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="20cbb-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="20cbb-137">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="20cbb-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

