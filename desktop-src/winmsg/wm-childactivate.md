---
description: Inviato a una finestra figlio quando l'utente fa clic sulla barra del titolo della finestra o quando la finestra è attivata, spostata o ridimensionata.
ms.assetid: 6e60725d-aa01-48bb-86a5-f17f56b97d35
title: Messaggio WM_CHILDACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82564a63cfbbbfe5e3693e331c8e990fa934e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757829"
---
# <a name="wm_childactivate-message"></a><span data-ttu-id="f855b-103">\_Messaggio CHILDACTIVATE WM</span><span class="sxs-lookup"><span data-stu-id="f855b-103">WM\_CHILDACTIVATE message</span></span>

<span data-ttu-id="f855b-104">Inviato a una finestra figlio quando l'utente fa clic sulla barra del titolo della finestra o quando la finestra è attivata, spostata o ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="f855b-104">Sent to a child window when the user clicks the window's title bar or when the window is activated, moved, or sized.</span></span>

<span data-ttu-id="f855b-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f855b-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHILDACTIVATE                0x0022
```



## <a name="parameters"></a><span data-ttu-id="f855b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f855b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f855b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f855b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f855b-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="f855b-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f855b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f855b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f855b-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="f855b-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f855b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f855b-111">Return value</span></span>

<span data-ttu-id="f855b-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="f855b-112">Type: **LRESULT**</span></span>

<span data-ttu-id="f855b-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="f855b-113">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f855b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f855b-114">Requirements</span></span>



| <span data-ttu-id="f855b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f855b-115">Requirement</span></span> | <span data-ttu-id="f855b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f855b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f855b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f855b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f855b-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f855b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f855b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f855b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f855b-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f855b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f855b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f855b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f855b-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f855b-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f855b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f855b-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="f855b-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f855b-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f855b-125">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="f855b-125">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="f855b-126">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="f855b-126">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

<span data-ttu-id="f855b-127">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f855b-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f855b-128">Windows</span><span class="sxs-lookup"><span data-stu-id="f855b-128">Windows</span></span>](windows.md)
</dt> </dl>

 

 
