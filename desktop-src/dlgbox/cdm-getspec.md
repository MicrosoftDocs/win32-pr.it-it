---
title: CDM_GETSPEC messaggio (Commdlg.h)
description: Recupera il nome del file (non incluso il percorso) del file attualmente selezionato in una finestra di dialogo Apri o Salva con nome in stile Esplora risorse.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- CDM_GETSPEC finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938536ea7cc72ebb950420ad3d5c9bd35c64db72
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590928"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="c6643-104">Messaggio \_ GETSPEC CDM</span><span class="sxs-lookup"><span data-stu-id="c6643-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="c6643-105">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="c6643-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="c6643-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="c6643-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="c6643-107">Recupera il nome del file (non incluso il percorso)  del file attualmente selezionato in una finestra di dialogo Apri o **Salva con** nome in stile Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="c6643-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="c6643-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c6643-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="c6643-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6643-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6643-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6643-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6643-111">Dimensione, in caratteri, del buffer *lParam.*</span><span class="sxs-lookup"><span data-stu-id="c6643-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c6643-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6643-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6643-113">Puntatore al buffer che riceve il nome del file.</span><span class="sxs-lookup"><span data-stu-id="c6643-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6643-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6643-114">Return value</span></span>

<span data-ttu-id="c6643-115">Se il messaggio ha esito positivo, il valore restituito è la dimensione, in caratteri, della stringa del nome file, incluso il carattere NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c6643-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="c6643-116">Si tratta del numero di byte o caratteri copiati nel buffer o della dimensione del buffer necessaria se il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="c6643-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="c6643-117">Se si verifica un errore, il valore restituito è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="c6643-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6643-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6643-118">Remarks</span></span>

<span data-ttu-id="c6643-119">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c6643-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="c6643-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6643-120">Requirements</span></span>



| <span data-ttu-id="c6643-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6643-121">Requirement</span></span> | <span data-ttu-id="c6643-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c6643-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6643-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6643-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c6643-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6643-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c6643-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6643-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c6643-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6643-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6643-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6643-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6643-128"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6643-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6643-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6643-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6643-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c6643-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6643-131">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="c6643-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="c6643-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="c6643-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="c6643-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="c6643-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="c6643-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c6643-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c6643-135">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="c6643-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

