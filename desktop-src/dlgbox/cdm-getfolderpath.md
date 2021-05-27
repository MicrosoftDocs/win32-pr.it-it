---
title: CDM_GETFOLDERPATH messaggio (Commdlg.h)
description: Recupera il percorso della cartella o della directory attualmente aperta per una finestra di dialogo Apri o Salva con nome in stile Esplora risorse.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96b8d25714dc3f8bdcf016ac1fd69b2af2414f0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550006"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="14c0c-104">Messaggio \_ CDM GETFOLDERPATH</span><span class="sxs-lookup"><span data-stu-id="14c0c-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="14c0c-105">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="14c0c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="14c0c-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="14c0c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="14c0c-107">Recupera il percorso della cartella o della directory  attualmente aperta per una finestra di dialogo Apri o **Salva con** nome in stile Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="14c0c-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="14c0c-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="14c0c-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="14c0c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="14c0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c0c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14c0c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14c0c-111">Dimensione, in caratteri, del buffer *lParam.*</span><span class="sxs-lookup"><span data-stu-id="14c0c-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="14c0c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14c0c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14c0c-113">Puntatore al buffer che riceve il percorso.</span><span class="sxs-lookup"><span data-stu-id="14c0c-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c0c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14c0c-114">Return value</span></span>

<span data-ttu-id="14c0c-115">Se il messaggio ha esito positivo, il valore restituito è la dimensione, in caratteri, della stringa di percorso, incluso il carattere Null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="14c0c-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="14c0c-116">Si tratta del numero di byte o caratteri copiati nel buffer o della dimensione del buffer necessaria se il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="14c0c-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="14c0c-117">Se si verifica un errore, il valore restituito è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="14c0c-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c0c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="14c0c-118">Remarks</span></span>

<span data-ttu-id="14c0c-119">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="14c0c-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="14c0c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14c0c-120">Requirements</span></span>



| <span data-ttu-id="14c0c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c0c-121">Requirement</span></span> | <span data-ttu-id="14c0c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="14c0c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c0c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14c0c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="14c0c-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14c0c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="14c0c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14c0c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="14c0c-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14c0c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14c0c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14c0c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c0c-128"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="14c0c-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c0c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14c0c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="14c0c-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="14c0c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14c0c-131">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="14c0c-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="14c0c-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="14c0c-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="14c0c-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="14c0c-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="14c0c-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="14c0c-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14c0c-135">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="14c0c-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

