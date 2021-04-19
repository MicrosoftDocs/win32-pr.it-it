---
title: Messaggio WM_CHOOSEFONT_GETLOGFONT (COMMDLG. h)
description: Un'applicazione invia il \_ messaggio WM ChooseFont \_ GETLOGFONT a una finestra di dialogo tipo di carattere per recuperare le informazioni sulle selezioni dei tipi di carattere correnti dell'utente.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Finestre di dialogo WM_CHOOSEFONT_GETLOGFONT messaggio
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302084"
---
# <a name="wm_choosefont_getlogfont-message"></a><span data-ttu-id="a3582-104">\_ \_ Messaggio GETLOGFONT di WM ChooseFont</span><span class="sxs-lookup"><span data-stu-id="a3582-104">WM\_CHOOSEFONT\_GETLOGFONT message</span></span>

<span data-ttu-id="a3582-105">Un'applicazione invia il messaggio **WM \_ ChooseFont \_ GETLOGFONT** a una finestra di dialogo tipo di **carattere** per recuperare le informazioni sulle selezioni dei tipi di carattere correnti dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a3582-105">An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a><span data-ttu-id="a3582-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3582-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3582-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3582-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a3582-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a3582-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3582-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3582-110">Puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che riceve informazioni sulle selezioni del tipo di carattere correnti dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a3582-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the user's current font selections.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3582-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3582-111">Return value</span></span>

<span data-ttu-id="a3582-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a3582-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3582-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3582-113">Remarks</span></span>

<span data-ttu-id="a3582-114">La funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea una finestra di dialogo del **tipo di carattere** .</span><span class="sxs-lookup"><span data-stu-id="a3582-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box.</span></span> <span data-ttu-id="a3582-115">Quando l'utente chiude la finestra di dialogo **tipo di carattere** , la funzione **ChooseFont** restituisce informazioni sulle selezioni del tipo di carattere dell'utente nella struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .</span><span class="sxs-lookup"><span data-stu-id="a3582-115">When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span> <span data-ttu-id="a3582-116">Il membro **LPLOGFONT** della struttura **ChooseFont** è un puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="a3582-116">The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

<span data-ttu-id="a3582-117">Usare il messaggio **WM \_ ChooseFont \_ GETLOGFONT** per ottenere informazioni sulle selezioni del tipo di carattere corrente dell'utente mentre è aperta la finestra di dialogo tipo di **carattere** .</span><span class="sxs-lookup"><span data-stu-id="a3582-117">Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open.</span></span> <span data-ttu-id="a3582-118">Se ad esempio si Abilita il pulsante **applica** nella finestra di dialogo **tipo di carattere** , inviare il messaggio per ottenere le informazioni sul tipo di carattere da applicare alla selezione di testo corrente.</span><span class="sxs-lookup"><span data-stu-id="a3582-118">For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.</span></span>

<span data-ttu-id="a3582-119">In genere, si abilita una procedura [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook per elaborare i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per il pulsante **applica** .</span><span class="sxs-lookup"><span data-stu-id="a3582-119">Typically, you enable a [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="a3582-120">Quando l'utente fa clic sul pulsante **applica** , la procedura hook invia il messaggio **WM \_ ChooseFont \_ GETLOGFONT** alla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a3582-120">When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3582-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3582-121">Requirements</span></span>



| <span data-ttu-id="a3582-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3582-122">Requirement</span></span> | <span data-ttu-id="a3582-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a3582-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3582-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3582-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a3582-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3582-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a3582-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3582-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a3582-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3582-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3582-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3582-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3582-129"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3582-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3582-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3582-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3582-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a3582-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a3582-132">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="a3582-132">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="a3582-133">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="a3582-133">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="a3582-134">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="a3582-134">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="a3582-135">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="a3582-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> <dt>

<span data-ttu-id="a3582-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a3582-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3582-137">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="a3582-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="a3582-138">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="a3582-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a3582-139">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="a3582-139">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

