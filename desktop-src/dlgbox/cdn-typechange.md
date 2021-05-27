---
title: CDN_TYPECHANGE di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse quando l'utente seleziona un nuovo tipo di file dalla casella combinata dei tipi di file.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE di dialogo del codice di notifica
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
ms.openlocfilehash: 3922dd71b70ace579fa4b5f2318776779afdfa4e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548866"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="da19c-104">Codice di notifica TYPECHANGE della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="da19c-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="da19c-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="da19c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="da19c-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="da19c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="da19c-107">Inviato da una finestra  di **dialogo** Apri o Salva con nome di tipo Esplora risorse quando l'utente seleziona un nuovo tipo di file dalla casella combinata dei tipi di file.</span><span class="sxs-lookup"><span data-stu-id="da19c-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="da19c-108">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="da19c-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="da19c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="da19c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da19c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da19c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da19c-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="da19c-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da19c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da19c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da19c-113">Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="da19c-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="da19c-114">La [**struttura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ TYPECHANGE della rete CDN.**</span><span class="sxs-lookup"><span data-stu-id="da19c-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="da19c-115">La [**struttura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene anche un puntatore a una struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) il cui membro **nFilterIndex** indica l'indice in base uno del filtro del tipo di file appena selezionato.</span><span class="sxs-lookup"><span data-stu-id="da19c-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da19c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da19c-116">Return value</span></span>

<span data-ttu-id="da19c-117">Questo messaggio non ha alcun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="da19c-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da19c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="da19c-118">Remarks</span></span>

<span data-ttu-id="da19c-119">Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="da19c-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="da19c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da19c-120">Requirements</span></span>



| <span data-ttu-id="da19c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="da19c-121">Requirement</span></span> | <span data-ttu-id="da19c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="da19c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da19c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da19c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da19c-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da19c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="da19c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da19c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da19c-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da19c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da19c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da19c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="da19c-128"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="da19c-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da19c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da19c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="da19c-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="da19c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da19c-131">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="da19c-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="da19c-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="da19c-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="da19c-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="da19c-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="da19c-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="da19c-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="da19c-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="da19c-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="da19c-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="da19c-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="da19c-137">Libreria di finestre di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="da19c-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

