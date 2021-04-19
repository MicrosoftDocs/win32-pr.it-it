---
title: CDN_HELP di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse quando l'utente fa clic sul pulsante ? .
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- CDN_HELP di dialogo del codice di notifica
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
ms.openlocfilehash: 5c03fae474f6622e1ccec0c5b52b0dfb473ba438
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590848"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="dddf3-104">Codice di notifica \_ della Guida della rete CDN</span><span class="sxs-lookup"><span data-stu-id="dddf3-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="dddf3-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="dddf3-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="dddf3-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="dddf3-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="dddf3-107">Inviato da una finestra di dialogo **Apri o** **Salva** con nome di tipo Esplora risorse quando l'utente fa clic sul **pulsante** ? .</span><span class="sxs-lookup"><span data-stu-id="dddf3-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="dddf3-108">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="dddf3-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="dddf3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dddf3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dddf3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dddf3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dddf3-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="dddf3-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dddf3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dddf3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dddf3-113">Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="dddf3-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="dddf3-114">La **struttura OFNOTIFY** contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica DELLA GUIDA della rete **CDN. \_**</span><span class="sxs-lookup"><span data-stu-id="dddf3-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dddf3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dddf3-115">Return value</span></span>

<span data-ttu-id="dddf3-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="dddf3-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="dddf3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="dddf3-117">Remarks</span></span>

<span data-ttu-id="dddf3-118">Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="dddf3-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dddf3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dddf3-119">Requirements</span></span>



| <span data-ttu-id="dddf3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dddf3-120">Requirement</span></span> | <span data-ttu-id="dddf3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dddf3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dddf3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dddf3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dddf3-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dddf3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dddf3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dddf3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dddf3-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dddf3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dddf3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dddf3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dddf3-127"><dt>Commdlg.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="dddf3-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dddf3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dddf3-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="dddf3-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="dddf3-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dddf3-130">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="dddf3-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="dddf3-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="dddf3-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="dddf3-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="dddf3-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="dddf3-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="dddf3-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="dddf3-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="dddf3-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="dddf3-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="dddf3-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dddf3-136">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="dddf3-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

