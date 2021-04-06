---
title: Messaggio CDM_GETFOLDERIDLIST (COMMDLG. h)
description: Recupera l'indirizzo dell'elenco di identificatori di elemento corrispondente alla cartella in cui è attualmente aperta una finestra di dialogo aperta o Salva con nome di tipo Esplora risorse.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- Finestre di dialogo CDM_GETFOLDERIDLIST messaggio
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
ms.openlocfilehash: 0b4ac82a628d6fcace6863abb30e5703af02a948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743207"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="25285-104">\_Messaggio GETFOLDERIDLIST CDM</span><span class="sxs-lookup"><span data-stu-id="25285-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="25285-105">\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25285-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="25285-106">È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]</span><span class="sxs-lookup"><span data-stu-id="25285-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="25285-107">Recupera l'indirizzo dell'elenco di identificatori di elemento corrispondente alla cartella in cui è attualmente aperta una finestra di dialogo **aperta** o **Salva con nome** di tipo Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="25285-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="25285-108">La finestra di dialogo deve essere stata creata con il flag **OFN \_ Explorer** . in caso contrario, il messaggio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="25285-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="25285-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="25285-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25285-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25285-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25285-111">Dimensione, in byte, del buffer *lParam* .</span><span class="sxs-lookup"><span data-stu-id="25285-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="25285-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25285-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25285-113">Puntatore al buffer che riceve l'elenco di identificatori di elemento.</span><span class="sxs-lookup"><span data-stu-id="25285-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25285-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25285-114">Return value</span></span>

<span data-ttu-id="25285-115">Se il messaggio ha esito positivo, il valore restituito è la dimensione, in byte, dell'elenco degli identificatori di elemento.</span><span class="sxs-lookup"><span data-stu-id="25285-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="25285-116">Si tratta del numero di byte copiati nel buffer o della dimensione del buffer necessaria se il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="25285-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="25285-117">Se si verifica un errore, il valore restituito è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="25285-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="25285-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="25285-118">Remarks</span></span>

<span data-ttu-id="25285-119">La macro corrispondente è la seguente:</span><span class="sxs-lookup"><span data-stu-id="25285-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="25285-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25285-120">Requirements</span></span>



| <span data-ttu-id="25285-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="25285-121">Requirement</span></span> | <span data-ttu-id="25285-122">Valore</span><span class="sxs-lookup"><span data-stu-id="25285-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25285-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25285-123">Minimum supported client</span></span><br/> | <span data-ttu-id="25285-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25285-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="25285-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25285-125">Minimum supported server</span></span><br/> | <span data-ttu-id="25285-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25285-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25285-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25285-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="25285-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25285-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25285-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25285-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="25285-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="25285-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="25285-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="25285-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="25285-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="25285-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="25285-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="25285-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="25285-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="25285-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25285-135">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="25285-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

