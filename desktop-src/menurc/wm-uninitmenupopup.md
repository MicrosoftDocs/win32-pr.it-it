---
title: Messaggio WM_UNINITMENUPOPUP (winuser. h)
description: Inviato quando un menu a discesa o un sottomenu viene eliminato definitivamente.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- Menu del messaggio WM_UNINITMENUPOPUP e altre risorse
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519190"
---
# <a name="wm_uninitmenupopup-message"></a><span data-ttu-id="6d699-104">\_Messaggio UNINITMENUPOPUP WM</span><span class="sxs-lookup"><span data-stu-id="6d699-104">WM\_UNINITMENUPOPUP message</span></span>

<span data-ttu-id="6d699-105">Inviato quando un menu a discesa o un sottomenu viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="6d699-105">Sent when a drop-down menu or submenu has been destroyed.</span></span>


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a><span data-ttu-id="6d699-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d699-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d699-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d699-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d699-108">Handle per il menu</span><span class="sxs-lookup"><span data-stu-id="6d699-108">A handle to the menu</span></span>

</dd> <dt>

<span data-ttu-id="6d699-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d699-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d699-110">La parola più ordinata identifica il menu che è stato eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="6d699-110">The high-order word identifies the menu that was destroyed.</span></span> <span data-ttu-id="6d699-111">Attualmente, questo parametro può essere solo **MF \_ SYSMENU** (il menu finestra).</span><span class="sxs-lookup"><span data-stu-id="6d699-111">Currently, this parameter can only be **MF\_SYSMENU** (the window menu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d699-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d699-112">Remarks</span></span>

<span data-ttu-id="6d699-113">Se un'applicazione riceve un messaggio [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) , riceverà un messaggio **WM \_ UNINITMENUPOPUP** .</span><span class="sxs-lookup"><span data-stu-id="6d699-113">If an application receives a [**WM\_INITMENUPOPUP**](wm-initmenupopup.md) message, it will receive a **WM\_UNINITMENUPOPUP** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d699-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d699-114">Requirements</span></span>



| <span data-ttu-id="6d699-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d699-115">Requirement</span></span> | <span data-ttu-id="6d699-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6d699-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d699-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d699-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d699-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d699-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6d699-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d699-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d699-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d699-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d699-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d699-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d699-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d699-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d699-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d699-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d699-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6d699-124">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="6d699-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d699-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6d699-126">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6d699-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6d699-127">Menu</span><span class="sxs-lookup"><span data-stu-id="6d699-127">Menus</span></span>](menus.md)
</dt> </dl>

 

