---
title: CDN_INCLUDEITEM codice di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome per determinare se la finestra di dialogo deve visualizzare un elemento nell'elenco di elementi di una cartella della shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM finestre di dialogo del codice di notifica
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a91c61e4a7c2786e67ed28e2c62e5963762659c
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590778"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="5f0c1-104">Codice di notifica \_ INCLUDEITEM della rete CDN</span><span class="sxs-lookup"><span data-stu-id="5f0c1-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="5f0c1-105">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="5f0c1-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="5f0c1-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="5f0c1-107">Inviato da una **finestra di dialogo** Apri o Salva con nome per determinare se la finestra di dialogo deve visualizzare un elemento nell'elenco di elementi di una cartella della shell. </span><span class="sxs-lookup"><span data-stu-id="5f0c1-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="5f0c1-108">Quando l'utente apre una cartella, la finestra di dialogo invia una notifica **\_ INCLUDEITEM della rete CDN** per ogni elemento nella cartella.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="5f0c1-109">La finestra di dialogo invia questa notifica solo se il flag **OFN \_ ENABLEINCLUDENOTIFY** è stato impostato al momento della creazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="5f0c1-110">La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="5f0c1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f0c1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0c1-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f0c1-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f0c1-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5f0c1-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f0c1-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f0c1-115">Puntatore a una [**struttura OFNOTIFYEX.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="5f0c1-116">La [**struttura OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) il cui membro **di** codice indica il messaggio di notifica **\_ INCLUDEITEM della rete CDN.**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="5f0c1-117">Il **membro psf** della struttura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) è un puntatore a un'interfaccia per la cartella i cui elementi vengono enumerati.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="5f0c1-118">Il **membro pidl** è un puntatore a un elenco di identificatori di elemento che identifica l'elemento relativo alla cartella.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0c1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f0c1-119">Return value</span></span>

<span data-ttu-id="5f0c1-120">Se la routine hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) restituisce zero, la finestra di dialogo esclude l'elemento dall'elenco di elementi.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="5f0c1-121">Per includere l'elemento, restituire un valore diverso da zero dalla routine hook.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f0c1-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f0c1-122">Remarks</span></span>

<span data-ttu-id="5f0c1-123">La finestra di dialogo include sempre gli elementi con gli attributi **SFGAO \_ FILESYSTEM** e **SFGAO \_ FILESYSANCESTOR,** indipendentemente dal valore restituito dalla rete **CDN \_ INCLUDEITEM**.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f0c1-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f0c1-124">Requirements</span></span>



| <span data-ttu-id="5f0c1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0c1-125">Requirement</span></span> | <span data-ttu-id="5f0c1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5f0c1-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0c1-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0c1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0c1-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5f0c1-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0c1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0c1-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f0c1-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f0c1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f0c1-132"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f0c1-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0c1-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f0c1-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f0c1-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f0c1-135">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="5f0c1-136">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="5f0c1-137">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="5f0c1-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="5f0c1-138">**OFNOTIFYEX**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="5f0c1-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f0c1-140">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="5f0c1-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

