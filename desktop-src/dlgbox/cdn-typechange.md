---
title: Codice di notifica CDN_TYPECHANGE (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando l'utente seleziona un nuovo tipo di file dalla casella combinata tipi di file.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- Finestre di dialogo CDN_TYPECHANGE codice di notifica
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64226c1ac15cb6b55c6c2e2de7264d726e6f3a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476673"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="b1ac4-104">Codice di notifica TYPECHANGE della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="b1ac4-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="b1ac4-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b1ac4-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="b1ac4-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="b1ac4-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b1ac4-107">Inviato da una finestra di dialogo **Apri** o **Salva con nome** in stile esploratore quando l'utente seleziona un nuovo tipo di file dalla casella combinata tipi di file.</span><span class="sxs-lookup"><span data-stu-id="b1ac4-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="b1ac4-108">La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b1ac4-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="b1ac4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1ac4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ac4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1ac4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ac4-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="b1ac4-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b1ac4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1ac4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ac4-113">Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="b1ac4-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="b1ac4-114">La struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ TYPECHANGE** della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="b1ac4-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="b1ac4-115">La struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene inoltre un puntatore a una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) il cui membro **nFilterIndex** indica l'indice in base uno del filtro del tipo di file appena selezionato.</span><span class="sxs-lookup"><span data-stu-id="b1ac4-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1ac4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1ac4-116">Return value</span></span>

<span data-ttu-id="b1ac4-117">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b1ac4-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1ac4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1ac4-118">Remarks</span></span>

<span data-ttu-id="b1ac4-119">Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="b1ac4-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1ac4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1ac4-120">Requirements</span></span>



| <span data-ttu-id="b1ac4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1ac4-121">Requirement</span></span> | <span data-ttu-id="b1ac4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b1ac4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ac4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1ac4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ac4-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1ac4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1ac4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1ac4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ac4-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1ac4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1ac4-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1ac4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1ac4-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1ac4-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ac4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1ac4-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1ac4-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b1ac4-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1ac4-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b1ac4-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b1ac4-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="b1ac4-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b1ac4-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="b1ac4-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="b1ac4-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b1ac4-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="b1ac4-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b1ac4-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="b1ac4-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b1ac4-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1ac4-137">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="b1ac4-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

