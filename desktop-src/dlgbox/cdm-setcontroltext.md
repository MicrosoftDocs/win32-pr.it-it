---
title: CDM_SETCONTROLTEXT messaggio (Commdlg.h)
description: Imposta il testo per il controllo specificato in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- CDM_SETCONTROLTEXT finestre di dialogo del messaggio
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
ms.openlocfilehash: 89c82a9144717224871caecf44da352a4e01cac2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550126"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="c08e7-104">Messaggio \_ CDM SETCONTROLTEXT</span><span class="sxs-lookup"><span data-stu-id="c08e7-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="c08e7-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c08e7-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="c08e7-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="c08e7-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="c08e7-107">Imposta il testo per il controllo specificato in una finestra di dialogo Apri **o** **Salva con** nome di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="c08e7-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="c08e7-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c08e7-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="c08e7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c08e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c08e7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c08e7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c08e7-111">Identificatore del controllo sul quale deve essere impostato il testo.</span><span class="sxs-lookup"><span data-stu-id="c08e7-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="c08e7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c08e7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c08e7-113">Nuovo testo per il controllo.</span><span class="sxs-lookup"><span data-stu-id="c08e7-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c08e7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c08e7-114">Return value</span></span>

<span data-ttu-id="c08e7-115">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c08e7-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c08e7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c08e7-116">Remarks</span></span>

<span data-ttu-id="c08e7-117">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c08e7-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="c08e7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c08e7-118">Requirements</span></span>



| <span data-ttu-id="c08e7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08e7-119">Requirement</span></span> | <span data-ttu-id="c08e7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c08e7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c08e7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c08e7-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c08e7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c08e7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c08e7-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c08e7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c08e7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c08e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c08e7-126"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c08e7-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c08e7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c08e7-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c08e7-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c08e7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c08e7-129">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="c08e7-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="c08e7-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="c08e7-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="c08e7-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="c08e7-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="c08e7-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c08e7-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c08e7-133">Libreria di finestre di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="c08e7-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

