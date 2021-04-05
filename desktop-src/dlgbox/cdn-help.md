---
title: Codice di notifica CDN_HELP (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando l'utente fa clic sul pulsante?.
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- Finestre di dialogo CDN_HELP codice di notifica
topic_type:
- apiref
api_name:
- CDN_HELP
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c73b690b1ac522a985ae121413804c4385e0f2cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120862"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="cb93a-104">Codice di notifica della guida della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="cb93a-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="cb93a-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cb93a-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="cb93a-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="cb93a-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="cb93a-107">Inviato da una finestra di dialogo **Apri** o **Salva con nome in** stile esploratore **quando l'utente** fa clic sul pulsante?.</span><span class="sxs-lookup"><span data-stu-id="cb93a-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="cb93a-108">La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cb93a-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="cb93a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb93a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb93a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb93a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb93a-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="cb93a-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb93a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb93a-113">Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="cb93a-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="cb93a-114">La struttura **OFNOTIFY** contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica della **\_ Guida** della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="cb93a-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb93a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb93a-115">Return value</span></span>

<span data-ttu-id="cb93a-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb93a-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb93a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb93a-117">Remarks</span></span>

<span data-ttu-id="cb93a-118">Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="cb93a-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb93a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb93a-119">Requirements</span></span>



| <span data-ttu-id="cb93a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb93a-120">Requirement</span></span> | <span data-ttu-id="cb93a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cb93a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb93a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb93a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb93a-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb93a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cb93a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb93a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb93a-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb93a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb93a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb93a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb93a-127"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb93a-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb93a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb93a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb93a-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="cb93a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb93a-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="cb93a-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="cb93a-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="cb93a-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="cb93a-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="cb93a-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="cb93a-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="cb93a-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="cb93a-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="cb93a-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="cb93a-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="cb93a-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cb93a-136">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="cb93a-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

