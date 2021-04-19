---
title: CDM_GETFOLDERIDLIST messaggio (Commdlg.h)
description: Recupera l'indirizzo dell'elenco di identificatori di elemento corrispondente alla cartella attualmente aperta in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d16b53c90c3efc874b8aeabd1b97938a1b21ec
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590908"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="d84b5-104">Messaggio CDM \_ GETFOLDERIDLIST</span><span class="sxs-lookup"><span data-stu-id="d84b5-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="d84b5-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="d84b5-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="d84b5-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="d84b5-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="d84b5-107">Recupera l'indirizzo dell'elenco di identificatori di elemento  corrispondente  alla cartella attualmente aperta in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="d84b5-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="d84b5-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d84b5-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="d84b5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d84b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d84b5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d84b5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d84b5-111">Dimensione, in byte, del buffer *lParam.*</span><span class="sxs-lookup"><span data-stu-id="d84b5-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d84b5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d84b5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d84b5-113">Puntatore al buffer che riceve l'elenco di identificatori di elemento.</span><span class="sxs-lookup"><span data-stu-id="d84b5-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d84b5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d84b5-114">Return value</span></span>

<span data-ttu-id="d84b5-115">Se il messaggio ha esito positivo, il valore restituito è la dimensione, in byte, dell'elenco di identificatori di elemento.</span><span class="sxs-lookup"><span data-stu-id="d84b5-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="d84b5-116">Si tratta del numero di byte copiati nel buffer o delle dimensioni del buffer richieste se il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="d84b5-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="d84b5-117">Se si verifica un errore, il valore restituito è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="d84b5-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d84b5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d84b5-118">Remarks</span></span>

<span data-ttu-id="d84b5-119">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="d84b5-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="d84b5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d84b5-120">Requirements</span></span>



| <span data-ttu-id="d84b5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d84b5-121">Requirement</span></span> | <span data-ttu-id="d84b5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d84b5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d84b5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d84b5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d84b5-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d84b5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d84b5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d84b5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d84b5-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d84b5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d84b5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d84b5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d84b5-128"><dt>Commdlg.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d84b5-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d84b5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d84b5-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d84b5-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d84b5-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d84b5-131">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="d84b5-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="d84b5-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="d84b5-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="d84b5-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="d84b5-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="d84b5-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d84b5-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d84b5-135">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="d84b5-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

