---
title: Codice di notifica CDN_FILEOK (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando l'utente specifica un nome di file e fa clic sul pulsante OK.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- Finestre di dialogo CDN_FILEOK codice di notifica
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302396"
---
# <a name="cdn_fileok-notification-code"></a><span data-ttu-id="a9eff-104">Codice di notifica FILEOK della rete CDN \_</span><span class="sxs-lookup"><span data-stu-id="a9eff-104">CDN\_FILEOK notification code</span></span>

<span data-ttu-id="a9eff-105">Inviato da una finestra di dialogo **Apri** o **Salva con nome in** stile esploratore quando l'utente specifica un nome di file e fa clic sul pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="a9eff-105">Sent by an Explorer-style **Open** or **Save As** dialog box when the user specifies a file name and clicks the **OK** button.</span></span>

<span data-ttu-id="a9eff-106">La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a9eff-106">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="a9eff-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9eff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9eff-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9eff-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9eff-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a9eff-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9eff-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9eff-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9eff-111">Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="a9eff-111">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="a9eff-112">La struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ FILEOK** della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="a9eff-112">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FILEOK** notification message.</span></span>

<span data-ttu-id="a9eff-113">La struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene anche un puntatore a una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) il cui membro **lpstrFile** specifica l'indirizzo del nome file selezionato.</span><span class="sxs-lookup"><span data-stu-id="a9eff-113">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **lpstrFile** member specifies the address of the selected file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9eff-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9eff-114">Return value</span></span>

<span data-ttu-id="a9eff-115">Se la routine hook restituisce zero, la finestra di dialogo accetta il nome file specificato e si chiude.</span><span class="sxs-lookup"><span data-stu-id="a9eff-115">If the hook procedure returns zero, the dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="a9eff-116">Per rifiutare il nome file specificato e forzare la finestra di dialogo in modo che rimanga aperta, restituire un valore diverso da zero dalla routine hook e chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare un valore **\_ MSGRESULT DWL** diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a9eff-116">To reject the specified file name and force the dialog box to remain open, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set a nonzero **DWL\_MSGRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9eff-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9eff-117">Remarks</span></span>

<span data-ttu-id="a9eff-118">Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="a9eff-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9eff-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9eff-119">Requirements</span></span>



| <span data-ttu-id="a9eff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9eff-120">Requirement</span></span> | <span data-ttu-id="a9eff-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a9eff-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9eff-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9eff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9eff-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9eff-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9eff-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9eff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9eff-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9eff-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9eff-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9eff-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9eff-127"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9eff-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9eff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9eff-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9eff-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a9eff-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9eff-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="a9eff-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="a9eff-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="a9eff-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="a9eff-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="a9eff-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="a9eff-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="a9eff-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="a9eff-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="a9eff-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="a9eff-135">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="a9eff-135">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="a9eff-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a9eff-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9eff-137">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="a9eff-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="a9eff-138">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="a9eff-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a9eff-139">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="a9eff-139">**WM\_NOTIFY**</span></span>](../controls/wm-notify.md)
</dt> </dl>

 

