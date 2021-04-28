---
title: WM_INITMENUPOPUP messaggio (Winuser.h)
description: "WM_INITMENUPOPUP messaggio: inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu."
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d850547d57596dd36b36b941d1782c2aee1f5b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092519"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="7b3ac-105">Messaggio \_ WM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="7b3ac-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="7b3ac-106">Inviato quando un menu a discesa o un sottomenu sta per diventare attivo.</span><span class="sxs-lookup"><span data-stu-id="7b3ac-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="7b3ac-107">In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu.</span><span class="sxs-lookup"><span data-stu-id="7b3ac-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="7b3ac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b3ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b3ac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b3ac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3ac-110">Handle per il menu a discesa o il sottomenu.</span><span class="sxs-lookup"><span data-stu-id="7b3ac-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="7b3ac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b3ac-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3ac-112">La parola meno ordinata specifica la posizione relativa in base zero della voce di menu che apre il menu a discesa o il sottomenu.</span><span class="sxs-lookup"><span data-stu-id="7b3ac-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="7b3ac-113">La parola più importante indica se il menu a discesa è il menu della finestra.</span><span class="sxs-lookup"><span data-stu-id="7b3ac-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="7b3ac-114">Se il menu è il menu della finestra, questo parametro è **TRUE**; in caso contrario, è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="7b3ac-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b3ac-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b3ac-115">Return value</span></span>

<span data-ttu-id="7b3ac-116">Se un'applicazione elabora questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="7b3ac-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3ac-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b3ac-117">Requirements</span></span>



| <span data-ttu-id="7b3ac-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b3ac-118">Requirement</span></span> | <span data-ttu-id="7b3ac-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7b3ac-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3ac-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b3ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b3ac-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b3ac-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7b3ac-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b3ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b3ac-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b3ac-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b3ac-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b3ac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b3ac-125"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ac-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3ac-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b3ac-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7b3ac-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7b3ac-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="7b3ac-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b3ac-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="7b3ac-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b3ac-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7b3ac-130">**WM \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="7b3ac-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="7b3ac-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7b3ac-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7b3ac-132">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="7b3ac-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

