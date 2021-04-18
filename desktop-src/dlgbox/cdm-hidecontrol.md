---
title: Messaggio CDM_HIDECONTROL (COMMDLG. h)
description: Nasconde il controllo specificato in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- Finestre di dialogo CDM_HIDECONTROL messaggio
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff632b7d1e3c24c84f73498846db9e6bfa68fd74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301719"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="44f16-104">\_Messaggio HIDECONTROL CDM</span><span class="sxs-lookup"><span data-stu-id="44f16-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="44f16-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44f16-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="44f16-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="44f16-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="44f16-107">Nasconde il controllo specificato in una finestra di dialogo **Apri** o **Salva con nome** di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="44f16-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="44f16-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ Explorer** . in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="44f16-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="44f16-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="44f16-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f16-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44f16-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44f16-111">Identificatore del controllo da nascondere.</span><span class="sxs-lookup"><span data-stu-id="44f16-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="44f16-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44f16-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44f16-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="44f16-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f16-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44f16-114">Return value</span></span>

<span data-ttu-id="44f16-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="44f16-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f16-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="44f16-116">Remarks</span></span>

<span data-ttu-id="44f16-117">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="44f16-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="44f16-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44f16-118">Requirements</span></span>



| <span data-ttu-id="44f16-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44f16-119">Requirement</span></span> | <span data-ttu-id="44f16-120">Valore</span><span class="sxs-lookup"><span data-stu-id="44f16-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f16-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44f16-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44f16-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44f16-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="44f16-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44f16-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44f16-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44f16-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44f16-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44f16-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f16-126"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44f16-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44f16-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44f16-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="44f16-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="44f16-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44f16-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="44f16-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="44f16-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="44f16-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="44f16-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="44f16-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="44f16-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="44f16-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="44f16-133">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="44f16-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

