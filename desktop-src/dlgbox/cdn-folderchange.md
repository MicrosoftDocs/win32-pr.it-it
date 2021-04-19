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
ms.openlocfilehash: b39075bddbd191f60a9f9bcbad745e213fe9a978
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590868"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="5d190-104">Codice di notifica FOLDERCHANGE della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="5d190-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="5d190-105">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="5d190-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="5d190-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="5d190-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="5d190-107">Inviato da una finestra di dialogo **Apri o** **Salva** con nome di tipo Esplora risorse quando viene aperta una nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="5d190-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="5d190-108">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="5d190-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="5d190-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d190-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d190-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d190-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d190-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5d190-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5d190-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d190-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d190-113">Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="5d190-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="5d190-114">La **struttura OFNOTIFY** contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro **di** codice indica il messaggio di notifica **\_ FOLDERCHANGE della rete CDN.**</span><span class="sxs-lookup"><span data-stu-id="5d190-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d190-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d190-115">Return value</span></span>

<span data-ttu-id="5d190-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="5d190-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d190-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d190-117">Remarks</span></span>

<span data-ttu-id="5d190-118">Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="5d190-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="5d190-119">Per ottenere il percorso della cartella appena aperta, la procedura hook può inviare il [**messaggio \_ CDM GETFOLDERPATH**](cdm-getfolderpath.md) alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5d190-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d190-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d190-120">Requirements</span></span>



| <span data-ttu-id="5d190-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d190-121">Requirement</span></span> | <span data-ttu-id="5d190-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5d190-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d190-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d190-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5d190-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d190-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5d190-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d190-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5d190-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d190-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d190-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d190-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d190-128"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d190-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d190-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d190-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d190-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5d190-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d190-131">**CDM \_ GETFOLDERPATH**</span><span class="sxs-lookup"><span data-stu-id="5d190-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="5d190-132">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="5d190-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="5d190-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="5d190-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="5d190-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="5d190-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="5d190-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="5d190-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="5d190-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5d190-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5d190-137">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="5d190-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

