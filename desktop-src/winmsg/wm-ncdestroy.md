---
description: Notifica a una finestra che la relativa area non client viene eliminata definitivamente. La funzione DestroyWindow invia il \_ messaggio WM NCDESTROY alla finestra che segue il \_ messaggio WM Destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Messaggio WM_NCDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967564"
---
# <a name="wm_ncdestroy-message"></a><span data-ttu-id="2ab38-104">\_Messaggio NCDESTROY WM</span><span class="sxs-lookup"><span data-stu-id="2ab38-104">WM\_NCDESTROY message</span></span>

<span data-ttu-id="2ab38-105">Notifica a una finestra che la relativa area non client viene eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="2ab38-105">Notifies a window that its nonclient area is being destroyed.</span></span> <span data-ttu-id="2ab38-106">La funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) invia il messaggio **WM \_ NCDESTROY** alla finestra che segue il messaggio [**WM \_ Destroy**](wm-destroy.md) .[**WM \_ Destroy**](wm-destroy.md) viene usato per liberare l'oggetto Memory allocato associato alla finestra.</span><span class="sxs-lookup"><span data-stu-id="2ab38-106">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function sends the **WM\_NCDESTROY** message to the window following the [**WM\_DESTROY**](wm-destroy.md) message.[**WM\_DESTROY**](wm-destroy.md) is used to free the allocated memory object associated with the window.</span></span>

<span data-ttu-id="2ab38-107">Il messaggio **WM \_ NCDESTROY** viene inviato dopo che le finestre figlio sono state eliminate definitivamente.</span><span class="sxs-lookup"><span data-stu-id="2ab38-107">The **WM\_NCDESTROY** message is sent after the child windows have been destroyed.</span></span> <span data-ttu-id="2ab38-108">Al contrario, [**WM \_ Destroy**](wm-destroy.md) viene inviato prima che vengano distrutte le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="2ab38-108">In contrast, [**WM\_DESTROY**](wm-destroy.md) is sent before the child windows are destroyed.</span></span>

<span data-ttu-id="2ab38-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2ab38-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a><span data-ttu-id="2ab38-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ab38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab38-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ab38-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ab38-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2ab38-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2ab38-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ab38-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ab38-114">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2ab38-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ab38-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ab38-115">Return value</span></span>

<span data-ttu-id="2ab38-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ab38-116">Type: **LRESULT**</span></span>

<span data-ttu-id="2ab38-117">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="2ab38-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab38-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ab38-118">Remarks</span></span>

<span data-ttu-id="2ab38-119">Questo messaggio libera la memoria allocata internamente per la finestra.</span><span class="sxs-lookup"><span data-stu-id="2ab38-119">This message frees any memory internally allocated for the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab38-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ab38-120">Requirements</span></span>



| <span data-ttu-id="2ab38-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ab38-121">Requirement</span></span> | <span data-ttu-id="2ab38-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2ab38-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab38-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ab38-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab38-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ab38-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2ab38-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ab38-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab38-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ab38-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2ab38-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ab38-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ab38-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ab38-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab38-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ab38-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ab38-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2ab38-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ab38-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="2ab38-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="2ab38-132">**eliminazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="2ab38-132">**WM\_DESTROY**</span></span>](wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="2ab38-133">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="2ab38-133">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="2ab38-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2ab38-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2ab38-135">Windows</span><span class="sxs-lookup"><span data-stu-id="2ab38-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
