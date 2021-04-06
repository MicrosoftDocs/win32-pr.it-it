---
title: Messaggio WM_CHOOSEFONT_SETLOGFONT (COMMDLG. h)
description: Un'applicazione invia il \_ messaggio WM ChooseFont \_ SETLOGFONT a una finestra di dialogo tipo di carattere per impostare le informazioni correnti sui caratteri logici.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Finestre di dialogo WM_CHOOSEFONT_SETLOGFONT messaggio
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742583"
---
# <a name="wm_choosefont_setlogfont-message"></a><span data-ttu-id="7be5c-104">\_ \_ Messaggio SETLOGFONT di WM ChooseFont</span><span class="sxs-lookup"><span data-stu-id="7be5c-104">WM\_CHOOSEFONT\_SETLOGFONT message</span></span>

<span data-ttu-id="7be5c-105">Un'applicazione invia il messaggio **WM \_ ChooseFont \_ SETLOGFONT** a una finestra di dialogo tipo di **carattere** per impostare le informazioni correnti sui caratteri logici.</span><span class="sxs-lookup"><span data-stu-id="7be5c-105">An application sends the **WM\_CHOOSEFONT\_SETLOGFONT** message to a **Font** dialog box to set the current logical font information.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a><span data-ttu-id="7be5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7be5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be5c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7be5c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7be5c-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="7be5c-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7be5c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7be5c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7be5c-110">Puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene informazioni sul tipo di carattere logico corrente.</span><span class="sxs-lookup"><span data-stu-id="7be5c-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the current logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be5c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7be5c-111">Return value</span></span>

<span data-ttu-id="7be5c-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="7be5c-112">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7be5c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7be5c-113">Remarks</span></span>

<span data-ttu-id="7be5c-114">Quando si chiama la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per creare una finestra di dialogo del **tipo di carattere** , è possibile usare il membro **LPLOGFONT** della struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) contenente i valori iniziali per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7be5c-114">When you call the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to create a **Font** dialog box, you can use the **lpLogFont** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure containing initial values for the dialog box.</span></span> <span data-ttu-id="7be5c-115">Usare il messaggio **WM \_ ChooseFont \_ SETLOGFONT** per specificare una struttura **LOGFONT** con valori diversi mentre è aperta la finestra di dialogo tipo di **carattere** .</span><span class="sxs-lookup"><span data-stu-id="7be5c-115">Use the **WM\_CHOOSEFONT\_SETLOGFONT** message to specify a **LOGFONT** structure with different values while the **Font** dialog box is open.</span></span>

<span data-ttu-id="7be5c-116">In genere, si invia il messaggio **WM \_ ChooseFont \_ SETLOGFONT** da una procedura di hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="7be5c-116">Typically, you would send the **WM\_CHOOSEFONT\_SETLOGFONT** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span> <span data-ttu-id="7be5c-117">La procedura hook può anche inviare i messaggi [**WM \_ ChooseFont \_ GETLOGFONT**](wm-choosefont-getlogfont.md) e [**WM \_ ChooseFont \_**](wm-choosefont-setflags.md) .</span><span class="sxs-lookup"><span data-stu-id="7be5c-117">The hook procedure can also send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be5c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7be5c-118">Requirements</span></span>



| <span data-ttu-id="7be5c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be5c-119">Requirement</span></span> | <span data-ttu-id="7be5c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7be5c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be5c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7be5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7be5c-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7be5c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7be5c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7be5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7be5c-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7be5c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7be5c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7be5c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be5c-126"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7be5c-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be5c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7be5c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7be5c-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7be5c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7be5c-129">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="7be5c-129">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="7be5c-130">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="7be5c-130">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="7be5c-131">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="7be5c-131">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="7be5c-132">**\_GETLOGFONT ChooseFont \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7be5c-132">**WM\_CHOOSEFONT\_GETLOGFONT**</span></span>](wm-choosefont-getlogfont.md)
</dt> <dt>

[<span data-ttu-id="7be5c-133">**\_flag ChooseFont \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7be5c-133">**WM\_CHOOSEFONT\_SETFLAGS**</span></span>](wm-choosefont-setflags.md)
</dt> <dt>

<span data-ttu-id="7be5c-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7be5c-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7be5c-135">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="7be5c-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="7be5c-136">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="7be5c-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7be5c-137">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="7be5c-137">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

