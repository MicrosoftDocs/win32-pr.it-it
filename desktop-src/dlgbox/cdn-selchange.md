---
title: CDN_SELCHANGE di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse quando la selezione cambia nella casella di riepilogo che visualizza il contenuto della cartella o della directory attualmente aperta.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE di dialogo del codice di notifica
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
ms.openlocfilehash: 8c21aa9dda117c74707b3c890ad96e017b45bcc0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549226"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="333b4-104">Codice di notifica \_ SELCHANGE della rete CDN</span><span class="sxs-lookup"><span data-stu-id="333b4-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="333b4-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="333b4-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="333b4-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="333b4-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="333b4-107">Inviato da una  finestra  di dialogo Apri o Salva con nome di tipo Esplora risorse quando la selezione cambia nella casella di riepilogo che visualizza il contenuto della cartella o della directory attualmente aperta.</span><span class="sxs-lookup"><span data-stu-id="333b4-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="333b4-108">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="333b4-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="333b4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="333b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="333b4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="333b4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="333b4-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="333b4-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="333b4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="333b4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="333b4-113">Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="333b4-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="333b4-114">La **struttura OFNOTIFY** contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro **di** codice indica il messaggio di **notifica \_ SELCHANGE della rete CDN.**</span><span class="sxs-lookup"><span data-stu-id="333b4-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="333b4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="333b4-115">Return value</span></span>

<span data-ttu-id="333b4-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="333b4-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="333b4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="333b4-117">Remarks</span></span>

<span data-ttu-id="333b4-118">Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="333b4-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="333b4-119">Per ottenere il nome del file o della cartella appena selezionata, la procedura hook può inviare il messaggio [**\_ CDM GETFILEPATH**](cdm-getfilepath.md) o [**CDM \_ GETSPEC**](cdm-getspec.md) alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="333b4-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="333b4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="333b4-120">Requirements</span></span>



| <span data-ttu-id="333b4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="333b4-121">Requirement</span></span> | <span data-ttu-id="333b4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="333b4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="333b4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="333b4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="333b4-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="333b4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="333b4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="333b4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="333b4-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="333b4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="333b4-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="333b4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="333b4-128"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="333b4-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="333b4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="333b4-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="333b4-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="333b4-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="333b4-131">**CDM \_ GETFILEPATH**</span><span class="sxs-lookup"><span data-stu-id="333b4-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="333b4-132">**CDM \_ GETSPEC**</span><span class="sxs-lookup"><span data-stu-id="333b4-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="333b4-133">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="333b4-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="333b4-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="333b4-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="333b4-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="333b4-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="333b4-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="333b4-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="333b4-137">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="333b4-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="333b4-138">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="333b4-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

