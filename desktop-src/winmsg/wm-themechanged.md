---
description: Trasmette a ogni finestra dopo un evento di modifica del tema. Esempi di eventi di modifica del tema sono l'attivazione di un tema, la disattivazione di un tema o una transizione da un tema a un altro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Messaggio WM_THEMECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751199"
---
# <a name="wm_themechanged-message"></a><span data-ttu-id="c5011-104">\_Messaggio THEMECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="c5011-104">WM\_THEMECHANGED message</span></span>

<span data-ttu-id="c5011-105">Trasmette a ogni finestra dopo un evento di modifica del tema.</span><span class="sxs-lookup"><span data-stu-id="c5011-105">Broadcast to every window following a theme change event.</span></span> <span data-ttu-id="c5011-106">Esempi di eventi di modifica del tema sono l'attivazione di un tema, la disattivazione di un tema o una transizione da un tema a un altro.</span><span class="sxs-lookup"><span data-stu-id="c5011-106">Examples of theme change events are the activation of a theme, the deactivation of a theme, or a transition from one theme to another.</span></span>


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a><span data-ttu-id="c5011-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5011-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5011-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5011-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5011-109">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="c5011-109">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c5011-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5011-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5011-111">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="c5011-111">This parameter is reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5011-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5011-112">Return value</span></span>

<span data-ttu-id="c5011-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c5011-113">Type: **LRESULT**</span></span>

<span data-ttu-id="c5011-114">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="c5011-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5011-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5011-115">Remarks</span></span>

<span data-ttu-id="c5011-116">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c5011-116">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="c5011-117">Questo messaggio viene pubblicato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c5011-117">This message is posted by the operating system.</span></span> <span data-ttu-id="c5011-118">Le applicazioni in genere non inviano questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="c5011-118">Applications typically do not send this message.</span></span>

 

<span data-ttu-id="c5011-119">I temi sono specifiche per l'aspetto dei controlli, in modo che l'elemento visivo di un controllo venga trattato separatamente dalla relativa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c5011-119">Themes are specifications for the appearance of controls, so that the visual element of a control is treated separately from its functionality.</span></span>

<span data-ttu-id="c5011-120">Per rilasciare un handle del tema esistente, chiamare [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span><span class="sxs-lookup"><span data-stu-id="c5011-120">To release an existing theme handle, call [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span></span> <span data-ttu-id="c5011-121">Per acquisire un nuovo handle del tema, usare [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="c5011-121">To acquire a new theme handle, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="c5011-122">Dopo la trasmissione **WM \_ THEMECHANGED** , gli eventuali handle di tema esistenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="c5011-122">Following the **WM\_THEMECHANGED** broadcast, any existing theme handles are invalid.</span></span> <span data-ttu-id="c5011-123">Una finestra sensibile al tema deve rilasciare e riaprire i relativi handle di tema preesistenti quando riceve il messaggio **\_ THEMECHANGED WM** .</span><span class="sxs-lookup"><span data-stu-id="c5011-123">A theme-aware window should release and reopen any of its pre-existing theme handles when it receives the **WM\_THEMECHANGED** message.</span></span> <span data-ttu-id="c5011-124">Se la funzione [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) restituisce **null**, la finestra deve disegnare senza tema.</span><span class="sxs-lookup"><span data-stu-id="c5011-124">If the [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) function returns **NULL**, the window should paint unthemed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5011-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5011-125">Requirements</span></span>



| <span data-ttu-id="c5011-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5011-126">Requirement</span></span> | <span data-ttu-id="c5011-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c5011-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5011-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5011-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c5011-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c5011-129">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c5011-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5011-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c5011-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5011-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5011-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5011-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5011-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5011-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5011-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5011-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5011-135">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="c5011-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c5011-136">**CloseThemeData**</span><span class="sxs-lookup"><span data-stu-id="c5011-136">**CloseThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[<span data-ttu-id="c5011-137">**IsThemeActive**</span><span class="sxs-lookup"><span data-stu-id="c5011-137">**IsThemeActive**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[<span data-ttu-id="c5011-138">**OpenThemeData**</span><span class="sxs-lookup"><span data-stu-id="c5011-138">**OpenThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
