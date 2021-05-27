---
title: CDN_INITDONE codice di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse quando il sistema ha terminato di disporre i controlli nella finestra di dialogo. Il sistema sposta i controlli standard per fare spazio ai controlli della finestra di dialogo figlio.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE finestre di dialogo del codice di notifica
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
ms.openlocfilehash: 6594c161d57a5d0772679477ee9bce2cda28ba12
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549836"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="a9b09-105">Codice di notifica \_ INITDONE della rete CDN</span><span class="sxs-lookup"><span data-stu-id="a9b09-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="a9b09-106">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="a9b09-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="a9b09-107">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="a9b09-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="a9b09-108">Inviato da una finestra  di dialogo **Apri** o Salva con nome di tipo Esplora risorse quando il sistema ha terminato di disporre i controlli nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a9b09-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="a9b09-109">Il sistema sposta i controlli standard per fare spazio ai controlli della finestra di dialogo figlio.</span><span class="sxs-lookup"><span data-stu-id="a9b09-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="a9b09-110">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="a9b09-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="a9b09-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9b09-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9b09-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9b09-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b09-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a9b09-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b09-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9b09-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b09-115">Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="a9b09-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="a9b09-116">La **struttura OFNOTIFY** contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di codice indica il messaggio di notifica **\_ INITDONE** della rete CDN. </span><span class="sxs-lookup"><span data-stu-id="a9b09-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9b09-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9b09-117">Return value</span></span>

<span data-ttu-id="a9b09-118">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a9b09-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b09-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9b09-119">Remarks</span></span>

<span data-ttu-id="a9b09-120">Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="a9b09-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b09-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9b09-121">Requirements</span></span>



| <span data-ttu-id="a9b09-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9b09-122">Requirement</span></span> | <span data-ttu-id="a9b09-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a9b09-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b09-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9b09-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b09-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9b09-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9b09-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9b09-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b09-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9b09-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9b09-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9b09-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b09-129"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9b09-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9b09-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9b09-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9b09-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a9b09-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9b09-132">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="a9b09-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="a9b09-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="a9b09-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="a9b09-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="a9b09-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="a9b09-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="a9b09-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="a9b09-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="a9b09-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="a9b09-137">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a9b09-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9b09-138">Libreria di finestre di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="a9b09-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

