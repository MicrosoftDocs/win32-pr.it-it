---
title: CDM_SETDEFEXT messaggio (Commdlg.h)
description: Imposta l'estensione di file predefinita per una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- CDM_SETDEFEXT finestre di dialogo del messaggio
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
ms.openlocfilehash: 0b0b1169a2777d5a5f82925366c6723af741706d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550116"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="4aabe-104">Messaggio \_ CDM SETDEFEXT</span><span class="sxs-lookup"><span data-stu-id="4aabe-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="4aabe-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="4aabe-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="4aabe-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="4aabe-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4aabe-107">Imposta l'estensione di file predefinita per una finestra di dialogo Apri **o** **Salva con** nome di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="4aabe-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="4aabe-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4aabe-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="4aabe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4aabe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aabe-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4aabe-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aabe-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="4aabe-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4aabe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4aabe-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aabe-113">Puntatore alla nuova estensione di file.</span><span class="sxs-lookup"><span data-stu-id="4aabe-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="4aabe-114">Non deve includere il punto (.).</span><span class="sxs-lookup"><span data-stu-id="4aabe-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aabe-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4aabe-115">Return value</span></span>

<span data-ttu-id="4aabe-116">Questo messaggio non ha alcun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="4aabe-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aabe-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4aabe-117">Remarks</span></span>

<span data-ttu-id="4aabe-118">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="4aabe-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="4aabe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4aabe-119">Requirements</span></span>



| <span data-ttu-id="4aabe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aabe-120">Requirement</span></span> | <span data-ttu-id="4aabe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4aabe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aabe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aabe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4aabe-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4aabe-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4aabe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aabe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4aabe-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4aabe-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4aabe-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4aabe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aabe-127"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aabe-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aabe-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4aabe-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="4aabe-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4aabe-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4aabe-130">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="4aabe-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="4aabe-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="4aabe-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="4aabe-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="4aabe-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="4aabe-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4aabe-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4aabe-134">Libreria di finestre di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="4aabe-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

