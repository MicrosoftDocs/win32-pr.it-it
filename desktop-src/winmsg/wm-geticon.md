---
description: Inviato a una finestra per recuperare un handle per l'icona grande o piccola associata a una finestra. Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Messaggio WM_GETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314862"
---
# <a name="wm_geticon-message"></a><span data-ttu-id="6f5fc-104">\_Messaggio WM GETicon</span><span class="sxs-lookup"><span data-stu-id="6f5fc-104">WM\_GETICON message</span></span>

<span data-ttu-id="6f5fc-105">Inviato a una finestra per recuperare un handle per l'icona grande o piccola associata a una finestra.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-105">Sent to a window to retrieve a handle to the large or small icon associated with a window.</span></span> <span data-ttu-id="6f5fc-106">Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-106">The system displays the large icon in the ALT+TAB dialog, and the small icon in the window caption.</span></span>

<span data-ttu-id="6f5fc-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6f5fc-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a><span data-ttu-id="6f5fc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f5fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f5fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f5fc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f5fc-110">Tipo di icona da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-110">The type of icon being retrieved.</span></span> <span data-ttu-id="6f5fc-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6f5fc-112">Valore</span><span class="sxs-lookup"><span data-stu-id="6f5fc-112">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="6f5fc-113">Significato</span><span class="sxs-lookup"><span data-stu-id="6f5fc-113">Meaning</span></span>                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="6f5fc-114"><dt>**Icona \_ di BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6f5fc-114"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="6f5fc-115">Recuperare l'icona grande per la finestra.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-115">Retrieve the large icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="6f5fc-116"><dt>**Icona \_ di PICCOLO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f5fc-116"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="6f5fc-117">Recuperare l'icona piccola per la finestra.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-117">Retrieve the small icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <span data-ttu-id="6f5fc-118"><dt>**Icona \_ di SMALL2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f5fc-118"><dt>**ICON\_SMALL2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="6f5fc-119">Recupera l'icona piccola fornita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-119">Retrieves the small icon provided by the application.</span></span> <span data-ttu-id="6f5fc-120">Se l'applicazione non ne fornisce uno, il sistema utilizza l'icona generata dal sistema per tale finestra.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-120">If the application does not provide one, the system uses the system-generated icon for that window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f5fc-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f5fc-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f5fc-122">Valore DPI dell'icona da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-122">The DPI of the icon being retrieved.</span></span> <span data-ttu-id="6f5fc-123">Questa operazione può essere utilizzata per fornire icone diverse a seconda delle dimensioni dell'icona.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-123">This can be used to provide different icons depending on the icon size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f5fc-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f5fc-124">Return value</span></span>

<span data-ttu-id="6f5fc-125">Tipo: **HICON**</span><span class="sxs-lookup"><span data-stu-id="6f5fc-125">Type: **HICON**</span></span>

<span data-ttu-id="6f5fc-126">Il valore restituito è un handle per l'icona grande o piccola, a seconda del valore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-126">The return value is a handle to the large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="6f5fc-127">Quando un'applicazione riceve questo messaggio, può restituire un handle a un'icona grande o piccola oppure passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="6f5fc-127">When an application receives this message, it can return a handle to a large or small icon, or pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f5fc-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f5fc-128">Remarks</span></span>

<span data-ttu-id="6f5fc-129">Quando un'applicazione riceve questo messaggio, può restituire un handle a un'icona grande o piccola oppure passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-129">When an application receives this message, it can return a handle to a large or small icon, or pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="6f5fc-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce un handle per l'icona grande o piccola associata alla finestra, a seconda del valore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns a handle to the large or small icon associated with the window, depending on the value of *wParam*.</span></span>

<span data-ttu-id="6f5fc-131">Una finestra priva di icona impostata in modo esplicito (con l' **\_ icona WM**) usa l'icona per la classe della finestra registrata e in questo caso [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituirà 0 per un messaggio **WM \_ GetIcon** .</span><span class="sxs-lookup"><span data-stu-id="6f5fc-131">A window that has no icon explicitly set (with **WM\_SETICON**) uses the icon for the registered window class, and in this case [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) will return 0 for a **WM\_GETICON** message.</span></span> <span data-ttu-id="6f5fc-132">Se l'invio di un messaggio **WM \_ GetIcon** a una finestra restituisce 0, provare a chiamare la funzione [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) per la finestra.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-132">If sending a **WM\_GETICON** message to a window returns 0, next try calling the [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) function for the window.</span></span> <span data-ttu-id="6f5fc-133">Se restituisce 0, provare la funzione [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) .</span><span class="sxs-lookup"><span data-stu-id="6f5fc-133">If that returns 0 then try the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f5fc-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f5fc-134">Requirements</span></span>



| <span data-ttu-id="6f5fc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5fc-135">Requirement</span></span> | <span data-ttu-id="6f5fc-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6f5fc-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5fc-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f5fc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6f5fc-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f5fc-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6f5fc-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f5fc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6f5fc-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f5fc-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f5fc-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f5fc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f5fc-142"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f5fc-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f5fc-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f5fc-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f5fc-144">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6f5fc-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f5fc-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6f5fc-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6f5fc-146">**ICONA di WM \_**</span><span class="sxs-lookup"><span data-stu-id="6f5fc-146">**WM\_SETICON**</span></span>](wm-seticon.md)
</dt> <dt>

<span data-ttu-id="6f5fc-147">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6f5fc-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f5fc-148">Windows</span><span class="sxs-lookup"><span data-stu-id="6f5fc-148">Windows</span></span>](windows.md)
</dt> </dl>

 

 
