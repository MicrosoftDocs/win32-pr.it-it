---
title: CDN_FOLDERCHANGE codice di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse quando viene aperta una nuova cartella.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- CDN_FOLDERCHANGE finestre di dialogo del codice di notifica
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
ms.openlocfilehash: 318aa2ffe4ddd47bcb1472f412f85ab785c5049e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550076"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="75ddf-104">Codice di notifica FOLDERCHANGE della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="75ddf-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="75ddf-105">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="75ddf-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="75ddf-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="75ddf-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="75ddf-107">Inviato da una finestra di dialogo **Apri o** **Salva** con nome di tipo Esplora risorse quando viene aperta una nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="75ddf-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="75ddf-108">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="75ddf-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="75ddf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="75ddf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ddf-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75ddf-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75ddf-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="75ddf-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="75ddf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75ddf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75ddf-113">Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="75ddf-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="75ddf-114">La **struttura OFNOTIFY** contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro **di** codice indica il messaggio di notifica **\_ FOLDERCHANGE della rete CDN.**</span><span class="sxs-lookup"><span data-stu-id="75ddf-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ddf-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75ddf-115">Return value</span></span>

<span data-ttu-id="75ddf-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="75ddf-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ddf-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="75ddf-117">Remarks</span></span>

<span data-ttu-id="75ddf-118">Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="75ddf-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="75ddf-119">Per ottenere il percorso della cartella appena aperta, la procedura hook può inviare il [**messaggio \_ CDM GETFOLDERPATH**](cdm-getfolderpath.md) alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="75ddf-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ddf-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75ddf-120">Requirements</span></span>



| <span data-ttu-id="75ddf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ddf-121">Requirement</span></span> | <span data-ttu-id="75ddf-122">Valore</span><span class="sxs-lookup"><span data-stu-id="75ddf-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ddf-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75ddf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="75ddf-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75ddf-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="75ddf-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75ddf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="75ddf-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75ddf-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75ddf-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75ddf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ddf-128"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="75ddf-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ddf-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75ddf-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="75ddf-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="75ddf-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75ddf-131">**CDM \_ GETFOLDERPATH**</span><span class="sxs-lookup"><span data-stu-id="75ddf-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="75ddf-132">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="75ddf-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="75ddf-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="75ddf-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="75ddf-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="75ddf-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="75ddf-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="75ddf-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="75ddf-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="75ddf-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75ddf-137">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="75ddf-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

