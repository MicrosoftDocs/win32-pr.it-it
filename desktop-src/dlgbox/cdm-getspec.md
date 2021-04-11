---
title: Messaggio CDM_GETSPEC (COMMDLG. h)
description: Recupera il nome file (senza includere il percorso) del file attualmente selezionato in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- Finestre di dialogo CDM_GETSPEC messaggio
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
ms.openlocfilehash: 2732bf2a8c581439a40538445853531b57cfc77a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118886"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="497a6-104">\_Messaggio CDM GETspec</span><span class="sxs-lookup"><span data-stu-id="497a6-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="497a6-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="497a6-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="497a6-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="497a6-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="497a6-107">Recupera il nome file (senza includere il percorso) del file attualmente selezionato in una finestra di dialogo **Apri** o **Salva con nome** di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="497a6-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="497a6-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ Explorer** . in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="497a6-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="497a6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="497a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="497a6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="497a6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="497a6-111">Dimensione, in caratteri, del buffer *lParam* .</span><span class="sxs-lookup"><span data-stu-id="497a6-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="497a6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="497a6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="497a6-113">Puntatore al buffer che riceve il nome del file.</span><span class="sxs-lookup"><span data-stu-id="497a6-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="497a6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="497a6-114">Return value</span></span>

<span data-ttu-id="497a6-115">Se il messaggio ha esito positivo, il valore restituito è la dimensione, in caratteri, della stringa del nome file, incluso il carattere NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="497a6-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="497a6-116">Si tratta del numero di byte o di caratteri copiati nel buffer o della dimensione del buffer necessaria se il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="497a6-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="497a6-117">Se si verifica un errore, il valore restituito è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="497a6-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="497a6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="497a6-118">Remarks</span></span>

<span data-ttu-id="497a6-119">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="497a6-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="497a6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="497a6-120">Requirements</span></span>



| <span data-ttu-id="497a6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="497a6-121">Requirement</span></span> | <span data-ttu-id="497a6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="497a6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="497a6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="497a6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="497a6-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="497a6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="497a6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="497a6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="497a6-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="497a6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="497a6-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="497a6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="497a6-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="497a6-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="497a6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="497a6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="497a6-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="497a6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="497a6-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="497a6-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="497a6-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="497a6-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="497a6-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="497a6-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="497a6-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="497a6-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="497a6-135">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="497a6-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

