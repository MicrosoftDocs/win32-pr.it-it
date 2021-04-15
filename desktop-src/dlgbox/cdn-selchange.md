---
title: Codice di notifica CDN_SELCHANGE (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando la selezione viene modificata nella casella di riepilogo in cui viene visualizzato il contenuto della cartella o della directory attualmente aperta.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- Finestre di dialogo CDN_SELCHANGE codice di notifica
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2f0f5a7860c7d729340a84bd80bc4e5713c733
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476678"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="ee741-104">Codice di notifica SelChange della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="ee741-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="ee741-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee741-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="ee741-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="ee741-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ee741-107">Inviato da una finestra di dialogo **Apri** o **Salva con nome** in stile esploratore quando la selezione viene modificata nella casella di riepilogo in cui viene visualizzato il contenuto della cartella o della directory attualmente aperta.</span><span class="sxs-lookup"><span data-stu-id="ee741-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="ee741-108">La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ee741-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="ee741-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee741-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee741-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee741-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee741-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="ee741-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee741-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee741-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee741-113">Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="ee741-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="ee741-114">La struttura **OFNOTIFY** contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ selChange** della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="ee741-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee741-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee741-115">Return value</span></span>

<span data-ttu-id="ee741-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ee741-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee741-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee741-117">Remarks</span></span>

<span data-ttu-id="ee741-118">Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="ee741-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="ee741-119">Per ottenere il nome del file o della cartella appena selezionata, la procedura hook può inviare il messaggio [**CDM \_ filePath**](cdm-getfilepath.md) o [**CDM \_ getspec**](cdm-getspec.md) alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ee741-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee741-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee741-120">Requirements</span></span>



| <span data-ttu-id="ee741-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee741-121">Requirement</span></span> | <span data-ttu-id="ee741-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ee741-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee741-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee741-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ee741-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee741-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ee741-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee741-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ee741-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee741-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ee741-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee741-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee741-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee741-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee741-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee741-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee741-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ee741-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee741-131">**CDM \_ filePath**</span><span class="sxs-lookup"><span data-stu-id="ee741-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="ee741-132">**CDM \_ GETspec**</span><span class="sxs-lookup"><span data-stu-id="ee741-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="ee741-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ee741-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="ee741-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="ee741-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="ee741-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="ee741-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="ee741-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="ee741-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="ee741-137">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ee741-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee741-138">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="ee741-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

