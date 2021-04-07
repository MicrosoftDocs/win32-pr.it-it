---
title: Messaggio CDM_SETDEFEXT (COMMDLG. h)
description: Imposta l'estensione di file predefinita per una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- Finestre di dialogo CDM_SETDEFEXT messaggio
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd722a5ae172e06879ae9aaafadc5180ee77867e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048617"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="98cda-104">\_Messaggio SETDEFEXT CDM</span><span class="sxs-lookup"><span data-stu-id="98cda-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="98cda-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98cda-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="98cda-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="98cda-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="98cda-107">Imposta l'estensione di file predefinita per una finestra di dialogo **Apri** o **Salva con** nome di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="98cda-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="98cda-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ Explorer** . in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="98cda-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="98cda-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="98cda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98cda-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98cda-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98cda-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="98cda-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98cda-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98cda-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98cda-113">Puntatore alla nuova estensione del nome di file.</span><span class="sxs-lookup"><span data-stu-id="98cda-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="98cda-114">Non deve includere il punto (.).</span><span class="sxs-lookup"><span data-stu-id="98cda-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98cda-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98cda-115">Return value</span></span>

<span data-ttu-id="98cda-116">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="98cda-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98cda-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="98cda-117">Remarks</span></span>

<span data-ttu-id="98cda-118">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="98cda-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="98cda-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98cda-119">Requirements</span></span>



| <span data-ttu-id="98cda-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="98cda-120">Requirement</span></span> | <span data-ttu-id="98cda-121">Valore</span><span class="sxs-lookup"><span data-stu-id="98cda-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98cda-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cda-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98cda-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98cda-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="98cda-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cda-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98cda-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98cda-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98cda-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98cda-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="98cda-127"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98cda-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98cda-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98cda-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="98cda-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="98cda-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98cda-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="98cda-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="98cda-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="98cda-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="98cda-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="98cda-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="98cda-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="98cda-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98cda-134">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="98cda-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

