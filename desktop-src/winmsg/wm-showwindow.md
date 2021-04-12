---
description: Inviato a una finestra quando la finestra sta per essere nascosta o visualizzata.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Messaggio WM_SHOWWINDOW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345571"
---
# <a name="wm_showwindow-message"></a><span data-ttu-id="9f530-103">\_Messaggio ShowWindow WM</span><span class="sxs-lookup"><span data-stu-id="9f530-103">WM\_SHOWWINDOW message</span></span>

<span data-ttu-id="9f530-104">Inviato a una finestra quando la finestra sta per essere nascosta o visualizzata.</span><span class="sxs-lookup"><span data-stu-id="9f530-104">Sent to a window when the window is about to be hidden or shown.</span></span>

<span data-ttu-id="9f530-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9f530-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a><span data-ttu-id="9f530-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f530-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f530-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f530-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f530-108">Indica se viene visualizzata una finestra.</span><span class="sxs-lookup"><span data-stu-id="9f530-108">Indicates whether a window is being shown.</span></span> <span data-ttu-id="9f530-109">Se *wParam* è **true**, viene visualizzata la finestra.</span><span class="sxs-lookup"><span data-stu-id="9f530-109">If *wParam* is **TRUE**, the window is being shown.</span></span> <span data-ttu-id="9f530-110">Se *wParam* è **false**, la finestra viene nascosta.</span><span class="sxs-lookup"><span data-stu-id="9f530-110">If *wParam* is **FALSE**, the window is being hidden.</span></span>

</dd> <dt>

<span data-ttu-id="9f530-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f530-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f530-112">Stato della finestra visualizzata.</span><span class="sxs-lookup"><span data-stu-id="9f530-112">The status of the window being shown.</span></span> <span data-ttu-id="9f530-113">Se *lParam* è zero, il messaggio è stato inviato a causa di una chiamata alla funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) . in caso contrario, *lParam* è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f530-113">If *lParam* is zero, the message was sent because of a call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function; otherwise, *lParam* is one of the following values.</span></span>



| <span data-ttu-id="9f530-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9f530-114">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="9f530-115">Significato</span><span class="sxs-lookup"><span data-stu-id="9f530-115">Meaning</span></span>                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <span data-ttu-id="9f530-116"><dt>**SW \_ OTHERUNZOOM**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9f530-116"><dt>**SW\_OTHERUNZOOM**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="9f530-117">È in corso il recupero della finestra perché una finestra di ingrandimento è stata ripristinata o ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="9f530-117">The window is being uncovered because a maximize window was restored or minimized.</span></span><br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <span data-ttu-id="9f530-118"><dt>**SW \_ OTHERZOOM**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9f530-118"><dt>**SW\_OTHERZOOM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="9f530-119">La finestra è coperta da un'altra finestra ingrandita.</span><span class="sxs-lookup"><span data-stu-id="9f530-119">The window is being covered by another window that has been maximized.</span></span><br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <span data-ttu-id="9f530-120"><dt>**SW \_ PARENTCLOSING**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9f530-120"><dt>**SW\_PARENTCLOSING**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="9f530-121">La finestra proprietaria della finestra viene ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="9f530-121">The window's owner window is being minimized.</span></span><br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <span data-ttu-id="9f530-122"><dt>**SW \_ PARENTOPENING**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9f530-122"><dt>**SW\_PARENTOPENING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="9f530-123">È in corso il ripristino della finestra proprietaria della finestra.</span><span class="sxs-lookup"><span data-stu-id="9f530-123">The window's owner window is being restored.</span></span><br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f530-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f530-124">Return value</span></span>

<span data-ttu-id="9f530-125">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9f530-125">Type: **LRESULT**</span></span>

<span data-ttu-id="9f530-126">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="9f530-126">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f530-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f530-127">Remarks</span></span>

<span data-ttu-id="9f530-128">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nasconde o Mostra la finestra, come specificato dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="9f530-128">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function hides or shows the window, as specified by the message.</span></span> <span data-ttu-id="9f530-129">Se una finestra ha lo stile di visualizzazione [**WS \_ visibile**](window-styles.md) quando viene creato, la finestra riceve questo messaggio dopo che è stato creato, ma prima che venga visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9f530-129">If a window has the [**WS\_VISIBLE**](window-styles.md) style when it is created, the window receives this message after it is created, but before it is displayed.</span></span> <span data-ttu-id="9f530-130">Una finestra riceve anche questo messaggio quando lo stato di visibilità viene modificato dalla funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) o [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) .</span><span class="sxs-lookup"><span data-stu-id="9f530-130">A window also receives this message when its visibility state is changed by the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) or [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) function.</span></span>

<span data-ttu-id="9f530-131">Il messaggio **WM \_ ShowWindow** non viene inviato nelle circostanze seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f530-131">The **WM\_SHOWWINDOW** message is not sent under the following circumstances:</span></span>

-   <span data-ttu-id="9f530-132">Quando viene creata una finestra sovrapposta di primo livello con lo stile [**WS \_ ingrandito**](window-styles.md) o **WS \_** .</span><span class="sxs-lookup"><span data-stu-id="9f530-132">When a top-level, overlapped window is created with the [**WS\_MAXIMIZE**](window-styles.md) or **WS\_MINIMIZE** style.</span></span>
-   <span data-ttu-id="9f530-133">Quando il flag **SW \_ SHOWNORMAL** viene specificato nella chiamata alla funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="9f530-133">When the **SW\_SHOWNORMAL** flag is specified in the call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f530-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f530-134">Requirements</span></span>



| <span data-ttu-id="9f530-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f530-135">Requirement</span></span> | <span data-ttu-id="9f530-136">Valore</span><span class="sxs-lookup"><span data-stu-id="9f530-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f530-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f530-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9f530-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f530-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9f530-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f530-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9f530-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f530-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f530-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f530-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f530-142"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f530-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f530-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f530-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f530-144">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9f530-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f530-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9f530-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9f530-146">**ShowOwnedPopups**</span><span class="sxs-lookup"><span data-stu-id="9f530-146">**ShowOwnedPopups**</span></span>](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[<span data-ttu-id="9f530-147">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="9f530-147">**ShowWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

<span data-ttu-id="9f530-148">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9f530-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9f530-149">Windows</span><span class="sxs-lookup"><span data-stu-id="9f530-149">Windows</span></span>](windows.md)
</dt> </dl>

 

 
