---
title: CDM_SETCONTROLTEXT messaggio (Commdlg.h)
description: Imposta il testo per il controllo specificato in una finestra di dialogo Apri o Salva con nome in stile Esplora risorse.
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
ms.openlocfilehash: 74d75bb3d3ac486bbb43545df80c67383a7655b8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590888"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="c4f19-104">Messaggio CDM \_ SETCONTROLTEXT</span><span class="sxs-lookup"><span data-stu-id="c4f19-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="c4f19-105">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="c4f19-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="c4f19-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="c4f19-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="c4f19-107">Imposta il testo per il controllo  specificato in una finestra di dialogo Apri o **Salva con** nome in stile Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="c4f19-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="c4f19-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c4f19-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="c4f19-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4f19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f19-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4f19-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f19-111">Identificatore del controllo su cui deve essere impostato il testo.</span><span class="sxs-lookup"><span data-stu-id="c4f19-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="c4f19-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4f19-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f19-113">Nuovo testo per il controllo.</span><span class="sxs-lookup"><span data-stu-id="c4f19-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f19-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4f19-114">Return value</span></span>

<span data-ttu-id="c4f19-115">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c4f19-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4f19-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4f19-116">Remarks</span></span>

<span data-ttu-id="c4f19-117">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c4f19-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="c4f19-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4f19-118">Requirements</span></span>



| <span data-ttu-id="c4f19-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4f19-119">Requirement</span></span> | <span data-ttu-id="c4f19-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c4f19-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f19-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4f19-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f19-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c4f19-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c4f19-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4f19-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f19-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c4f19-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4f19-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4f19-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4f19-126"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4f19-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4f19-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4f19-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4f19-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c4f19-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4f19-129">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="c4f19-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="c4f19-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="c4f19-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="c4f19-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="c4f19-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="c4f19-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c4f19-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c4f19-133">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="c4f19-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

