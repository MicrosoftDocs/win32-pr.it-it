---
title: Codice di notifica CDN_FOLDERCHANGE (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando viene aperta una nuova cartella.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- Finestre di dialogo CDN_FOLDERCHANGE codice di notifica
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c93bd37afa44e7fc5ca81d928974f56bf80d1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119947"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="4fc4e-104">Codice di notifica FOLDERCHANGE della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="4fc4e-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="4fc4e-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4fc4e-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="4fc4e-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="4fc4e-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4fc4e-107">Inviato da una finestra di dialogo **Apri** o **Salva con nome in** stile esploratore quando viene aperta una nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="4fc4e-108">La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4fc4e-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="4fc4e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fc4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc4e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fc4e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc4e-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4fc4e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fc4e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc4e-113">Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="4fc4e-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="4fc4e-114">La struttura **OFNOTIFY** contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ FOLDERCHANGE** della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc4e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fc4e-115">Return value</span></span>

<span data-ttu-id="4fc4e-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fc4e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fc4e-117">Remarks</span></span>

<span data-ttu-id="4fc4e-118">Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="4fc4e-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="4fc4e-119">Per ottenere il percorso della cartella appena aperta, la procedura hook può inviare il messaggio [**\_ GETFOLDERPATH CDM**](cdm-getfolderpath.md) alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4fc4e-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc4e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fc4e-120">Requirements</span></span>



| <span data-ttu-id="4fc4e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fc4e-121">Requirement</span></span> | <span data-ttu-id="4fc4e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4fc4e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc4e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fc4e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc4e-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fc4e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4fc4e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fc4e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc4e-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fc4e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4fc4e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fc4e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc4e-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fc4e-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc4e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fc4e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4fc4e-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4fc4e-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4fc4e-131">**\_GETFOLDERPATH CDM**</span><span class="sxs-lookup"><span data-stu-id="4fc4e-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="4fc4e-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="4fc4e-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="4fc4e-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="4fc4e-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="4fc4e-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="4fc4e-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="4fc4e-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="4fc4e-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="4fc4e-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4fc4e-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4fc4e-137">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="4fc4e-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

