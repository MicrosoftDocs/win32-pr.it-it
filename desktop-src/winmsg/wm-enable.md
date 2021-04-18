---
description: Inviato quando un'applicazione modifica lo stato di abilitazione di una finestra.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Messaggio WM_ENABLE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314870"
---
# <a name="wm_enable-message"></a><span data-ttu-id="dce2e-103">\_Messaggio di abilitazione WM</span><span class="sxs-lookup"><span data-stu-id="dce2e-103">WM\_ENABLE message</span></span>

<span data-ttu-id="dce2e-104">Inviato quando un'applicazione modifica lo stato di abilitazione di una finestra.</span><span class="sxs-lookup"><span data-stu-id="dce2e-104">Sent when an application changes the enabled state of a window.</span></span> <span data-ttu-id="dce2e-105">Viene inviata alla finestra il cui stato abilitato è in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="dce2e-105">It is sent to the window whose enabled state is changing.</span></span> <span data-ttu-id="dce2e-106">Questo messaggio viene inviato prima della restituzione della funzione [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) , ma dopo la modifica dello stato abilitato ([**WS \_ disabled**](window-styles.md) Style bit) della finestra.</span><span class="sxs-lookup"><span data-stu-id="dce2e-106">This message is sent before the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function returns, but after the enabled state ([**WS\_DISABLED**](window-styles.md) style bit) of the window has changed.</span></span>

<span data-ttu-id="dce2e-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dce2e-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a><span data-ttu-id="dce2e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dce2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce2e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dce2e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dce2e-110">Indica se la finestra è stata abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="dce2e-110">Indicates whether the window has been enabled or disabled.</span></span> <span data-ttu-id="dce2e-111">Questo parametro è **true** se la finestra è stata abilitata o **false** se la finestra è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="dce2e-111">This parameter is **TRUE** if the window has been enabled or **FALSE** if the window has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="dce2e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dce2e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dce2e-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="dce2e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce2e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dce2e-114">Return value</span></span>

<span data-ttu-id="dce2e-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="dce2e-115">Type: **LRESULT**</span></span>

<span data-ttu-id="dce2e-116">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="dce2e-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce2e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dce2e-117">Requirements</span></span>



| <span data-ttu-id="dce2e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dce2e-118">Requirement</span></span> | <span data-ttu-id="dce2e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dce2e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce2e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce2e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dce2e-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dce2e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dce2e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce2e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dce2e-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dce2e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dce2e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dce2e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce2e-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dce2e-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce2e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dce2e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="dce2e-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="dce2e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dce2e-128">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="dce2e-128">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

<span data-ttu-id="dce2e-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="dce2e-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dce2e-130">Windows</span><span class="sxs-lookup"><span data-stu-id="dce2e-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
