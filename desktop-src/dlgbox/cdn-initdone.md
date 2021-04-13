---
title: Codice di notifica CDN_INITDONE (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando il sistema ha completato la disposizione dei controlli nella finestra di dialogo. Il sistema sposta i controlli standard per creare spazio per i controlli della finestra di dialogo figlio.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- Finestre di dialogo CDN_INITDONE codice di notifica
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6d51f1c34a0a399775e1786356aae4fc6526fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400619"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="96684-105">Codice di notifica INITDONE della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="96684-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="96684-106">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="96684-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="96684-107">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="96684-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="96684-108">Inviato da una finestra di dialogo **Apri** o **Salva con nome** in stile esploratore quando il sistema ha completato la disposizione dei controlli nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="96684-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="96684-109">Il sistema sposta i controlli standard per creare spazio per i controlli della finestra di dialogo figlio.</span><span class="sxs-lookup"><span data-stu-id="96684-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="96684-110">La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="96684-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="96684-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="96684-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96684-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96684-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96684-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="96684-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="96684-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96684-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96684-115">Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="96684-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="96684-116">La struttura **OFNOTIFY** contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ INITDONE** della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="96684-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96684-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96684-117">Return value</span></span>

<span data-ttu-id="96684-118">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="96684-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="96684-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="96684-119">Remarks</span></span>

<span data-ttu-id="96684-120">Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="96684-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="96684-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96684-121">Requirements</span></span>



| <span data-ttu-id="96684-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="96684-122">Requirement</span></span> | <span data-ttu-id="96684-123">Valore</span><span class="sxs-lookup"><span data-stu-id="96684-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96684-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96684-124">Minimum supported client</span></span><br/> | <span data-ttu-id="96684-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96684-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="96684-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96684-126">Minimum supported server</span></span><br/> | <span data-ttu-id="96684-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96684-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96684-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96684-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="96684-129"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96684-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96684-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96684-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="96684-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="96684-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96684-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="96684-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="96684-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="96684-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="96684-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="96684-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="96684-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="96684-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="96684-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="96684-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="96684-137">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="96684-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="96684-138">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="96684-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

