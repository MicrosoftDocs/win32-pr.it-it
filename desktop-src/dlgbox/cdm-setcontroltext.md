---
title: Messaggio CDM_SETCONTROLTEXT (COMMDLG. h)
description: Imposta il testo per il controllo specificato in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- Finestre di dialogo CDM_SETCONTROLTEXT messaggio
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87490ba20b5785da4fb9660d97b1b9232d047671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400196"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="705f4-104">\_Messaggio SETCONTROLTEXT CDM</span><span class="sxs-lookup"><span data-stu-id="705f4-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="705f4-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="705f4-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="705f4-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="705f4-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="705f4-107">Imposta il testo per il controllo specificato in una finestra di dialogo **Apri** o **Salva con nome** di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="705f4-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="705f4-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ Explorer** . in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="705f4-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="705f4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="705f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="705f4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="705f4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="705f4-111">Identificatore del controllo il cui testo deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="705f4-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="705f4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="705f4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="705f4-113">Nuovo testo per il controllo.</span><span class="sxs-lookup"><span data-stu-id="705f4-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="705f4-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="705f4-114">Return value</span></span>

<span data-ttu-id="705f4-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="705f4-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="705f4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="705f4-116">Remarks</span></span>

<span data-ttu-id="705f4-117">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="705f4-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="705f4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="705f4-118">Requirements</span></span>



| <span data-ttu-id="705f4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="705f4-119">Requirement</span></span> | <span data-ttu-id="705f4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="705f4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705f4-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="705f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="705f4-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="705f4-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="705f4-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="705f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="705f4-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="705f4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="705f4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="705f4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="705f4-126"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="705f4-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="705f4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="705f4-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="705f4-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="705f4-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="705f4-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="705f4-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="705f4-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="705f4-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="705f4-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="705f4-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="705f4-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="705f4-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="705f4-133">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="705f4-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

