---
title: Messaggio WM_CHOOSEFONT_SETFLAGS (COMMDLG. h)
description: Un'applicazione invia il \_ \_ messaggio di flag ChooseFont di WM a una finestra di dialogo tipo di carattere per impostare le opzioni di visualizzazione per la finestra di dialogo.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Finestre di dialogo WM_CHOOSEFONT_SETFLAGS messaggio
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120571"
---
# <a name="wm_choosefont_setflags-message"></a><span data-ttu-id="fe211-104">Messaggio di FLAG di WM \_ ChooseFont \_</span><span class="sxs-lookup"><span data-stu-id="fe211-104">WM\_CHOOSEFONT\_SETFLAGS message</span></span>

<span data-ttu-id="fe211-105">Un'applicazione invia il messaggio di **\_ \_ flag ChooseFont di WM** a una finestra di dialogo **tipo di carattere** per impostare le opzioni di visualizzazione per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="fe211-105">An application sends the **WM\_CHOOSEFONT\_SETFLAGS** message to a **Font** dialog box to set the display options for the dialog box.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a><span data-ttu-id="fe211-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe211-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe211-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe211-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe211-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="fe211-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe211-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe211-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe211-110">Puntatore a una struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contenente nuove impostazioni nel membro dei **flag** .</span><span class="sxs-lookup"><span data-stu-id="fe211-110">A pointer to a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that contains new settings in the **Flags** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe211-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe211-111">Return value</span></span>

<span data-ttu-id="fe211-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="fe211-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe211-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe211-113">Remarks</span></span>

<span data-ttu-id="fe211-114">La funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea una finestra di dialogo del **tipo di carattere** e usa una struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare i valori iniziali per il membro dei **flag** .</span><span class="sxs-lookup"><span data-stu-id="fe211-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box and uses a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify the initial values for the **Flags** member.</span></span> <span data-ttu-id="fe211-115">Utilizzare il messaggio di **\_ \_ flag ChooseFont di WM** per specificare valori diversi per il membro dei **flag** mentre è aperta la finestra di dialogo **tipo di carattere** .</span><span class="sxs-lookup"><span data-stu-id="fe211-115">Use the **WM\_CHOOSEFONT\_SETFLAGS** message to specify different values for the **Flags** member while the **Font** dialog box is open.</span></span>

<span data-ttu-id="fe211-116">In genere, è necessario inviare il messaggio di **\_ \_ flag ChooseFont di WM** da una procedura di hook di [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="fe211-116">Typically, you should send the **WM\_CHOOSEFONT\_SETFLAGS** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe211-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe211-117">Requirements</span></span>



| <span data-ttu-id="fe211-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe211-118">Requirement</span></span> | <span data-ttu-id="fe211-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fe211-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe211-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe211-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe211-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe211-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fe211-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe211-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe211-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe211-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe211-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe211-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe211-125"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe211-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe211-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe211-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe211-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fe211-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fe211-128">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="fe211-128">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="fe211-129">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="fe211-129">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="fe211-130">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="fe211-130">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

<span data-ttu-id="fe211-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="fe211-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fe211-132">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="fe211-132">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

