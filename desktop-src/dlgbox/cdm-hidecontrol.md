---
title: CDM_HIDECONTROL messaggio (Commdlg.h)
description: Nasconde il controllo specificato in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- CDM_HIDECONTROL finestre di dialogo del messaggio
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
ms.openlocfilehash: 7c0f2f41017373d9064da8f1024066f131063d9d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590878"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="3646e-104">Messaggio HIDECONTROL di CDM \_</span><span class="sxs-lookup"><span data-stu-id="3646e-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="3646e-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="3646e-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="3646e-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="3646e-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="3646e-107">Nasconde il controllo specificato in  una finestra di dialogo Apri o **Salva con nome** di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="3646e-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="3646e-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3646e-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="3646e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3646e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3646e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3646e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3646e-111">Identificatore del controllo da nascondere.</span><span class="sxs-lookup"><span data-stu-id="3646e-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="3646e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3646e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3646e-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3646e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3646e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3646e-114">Return value</span></span>

<span data-ttu-id="3646e-115">Questo messaggio non ha alcun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3646e-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3646e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3646e-116">Remarks</span></span>

<span data-ttu-id="3646e-117">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="3646e-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="3646e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3646e-118">Requirements</span></span>



| <span data-ttu-id="3646e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3646e-119">Requirement</span></span> | <span data-ttu-id="3646e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3646e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3646e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3646e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3646e-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3646e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3646e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3646e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3646e-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3646e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3646e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3646e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3646e-126"><dt>Commdlg.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3646e-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3646e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3646e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3646e-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3646e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3646e-129">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="3646e-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="3646e-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="3646e-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="3646e-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="3646e-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="3646e-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3646e-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3646e-133">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="3646e-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

