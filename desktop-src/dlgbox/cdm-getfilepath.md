---
title: Messaggio CDM_GETFILEPATH (COMMDLG. h)
description: Recupera il percorso e il nome file del file selezionato in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- Finestre di dialogo CDM_GETFILEPATH messaggio
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b7cc278d1d5a2305b3d2a311ce9c82886f9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964696"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="b92a0-104">\_Messaggio CDM FilePath</span><span class="sxs-lookup"><span data-stu-id="b92a0-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="b92a0-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b92a0-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="b92a0-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="b92a0-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b92a0-107">Recupera il percorso e il nome file del file selezionato in una finestra di dialogo **Apri** o **Salva con** nome di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="b92a0-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="b92a0-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ Explorer** . in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b92a0-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="b92a0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b92a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b92a0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b92a0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b92a0-111">Dimensione, in caratteri, del buffer *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b92a0-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="b92a0-112">Per la versione ANSI, questo è il numero di byte; per la versione Unicode, questo è il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="b92a0-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="b92a0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b92a0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b92a0-114">Puntatore al buffer che riceve il nome e il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="b92a0-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b92a0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b92a0-115">Return value</span></span>

<span data-ttu-id="b92a0-116">Se il messaggio ha esito positivo, il valore restituito è la dimensione, in caratteri, del nome file e della stringa di percorso, incluso il carattere NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="b92a0-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="b92a0-117">Si tratta del numero di byte o di caratteri copiati nel buffer o della dimensione del buffer necessaria se il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="b92a0-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="b92a0-118">Se si verifica un errore, il valore restituito è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="b92a0-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b92a0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b92a0-119">Remarks</span></span>

<span data-ttu-id="b92a0-120">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b92a0-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="b92a0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b92a0-121">Requirements</span></span>



| <span data-ttu-id="b92a0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92a0-122">Requirement</span></span> | <span data-ttu-id="b92a0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b92a0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92a0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b92a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b92a0-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b92a0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b92a0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b92a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b92a0-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b92a0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b92a0-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b92a0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b92a0-129"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b92a0-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b92a0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b92a0-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="b92a0-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b92a0-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b92a0-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b92a0-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b92a0-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="b92a0-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b92a0-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b92a0-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="b92a0-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b92a0-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b92a0-136">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="b92a0-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

