---
description: Inviato a una finestra quando è necessario modificare l'area non client per indicare uno stato attivo o inattivo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Messaggio WM_NCACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312370"
---
# <a name="wm_ncactivate-message"></a><span data-ttu-id="8872a-103">\_Messaggio NCACTIVATE WM</span><span class="sxs-lookup"><span data-stu-id="8872a-103">WM\_NCACTIVATE message</span></span>

<span data-ttu-id="8872a-104">Inviato a una finestra quando è necessario modificare l'area non client per indicare uno stato attivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="8872a-104">Sent to a window when its nonclient area needs to be changed to indicate an active or inactive state.</span></span>

<span data-ttu-id="8872a-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8872a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a><span data-ttu-id="8872a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8872a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8872a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8872a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8872a-108">Indica quando è necessario modificare una barra del titolo o un'icona per indicare uno stato attivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="8872a-108">Indicates when a title bar or icon needs to be changed to indicate an active or inactive state.</span></span> <span data-ttu-id="8872a-109">Se è necessario disegnare una barra del titolo o un'icona attiva, il parametro *wParam* è **true**.</span><span class="sxs-lookup"><span data-stu-id="8872a-109">If an active title bar or icon is to be drawn, the *wParam* parameter is **TRUE**.</span></span> <span data-ttu-id="8872a-110">Se è necessario disegnare una barra del titolo o un'icona inattiva, *wParam* è **false**.</span><span class="sxs-lookup"><span data-stu-id="8872a-110">If an inactive title bar or icon is to be drawn, *wParam* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8872a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8872a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8872a-112">Quando uno [stile di visualizzazione](../controls/themes-overview.md) è attivo per questa finestra, questo parametro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8872a-112">When a [visual style](../controls/themes-overview.md) is active for this window, this parameter is not used.</span></span>

<span data-ttu-id="8872a-113">Quando uno stile di visualizzazione non è attivo per questa finestra, questo parametro è un handle per un'area di aggiornamento facoltativa per l'area non client della finestra.</span><span class="sxs-lookup"><span data-stu-id="8872a-113">When a visual style is not active for this window, this parameter is a handle to an optional update region for the nonclient area of the window.</span></span> <span data-ttu-id="8872a-114">Se questo parametro è impostato su-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non ridisegna l'area non client per riflettere la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="8872a-114">If this parameter is set to -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not repaint the nonclient area to reflect the state change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8872a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8872a-115">Return value</span></span>

<span data-ttu-id="8872a-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="8872a-116">Type: **LRESULT**</span></span>

<span data-ttu-id="8872a-117">Quando il parametro *wParam* è **false**, un'applicazione deve restituire **true** per indicare che il sistema deve procedere con l'elaborazione predefinita oppure deve restituire **false** per evitare la modifica.</span><span class="sxs-lookup"><span data-stu-id="8872a-117">When the *wParam* parameter is **FALSE**, an application should return **TRUE** to indicate that the system should proceed with the default processing, or it should return **FALSE** to prevent the change.</span></span> <span data-ttu-id="8872a-118">Quando *wParam* è **true**, il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8872a-118">When *wParam* is **TRUE**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8872a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8872a-119">Remarks</span></span>

<span data-ttu-id="8872a-120">Non è consigliabile elaborare i messaggi correlati all'area non client di una finestra standard, perché l'applicazione deve essere in grado di creare tutte le parti necessarie dell'area non client per la finestra.</span><span class="sxs-lookup"><span data-stu-id="8872a-120">Processing messages related to the nonclient area of a standard window is not recommended, because the application must be able to draw all the required parts of the nonclient area for the window.</span></span> <span data-ttu-id="8872a-121">Se un'applicazione elabora il messaggio, deve restituire **true** per indicare al sistema di completare la modifica della finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="8872a-121">If an application does process this message, it must return **TRUE** to direct the system to complete the change of active window.</span></span> <span data-ttu-id="8872a-122">Se la finestra è ridotta a icona quando viene ricevuto questo messaggio, l'applicazione deve passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="8872a-122">If the window is minimized when this message is received, the application should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="8872a-123">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna la barra del titolo o il titolo dell'icona nei colori attivi quando il parametro *wParam* è **true** e nei colori inattivi quando *wParam* è **false**.</span><span class="sxs-lookup"><span data-stu-id="8872a-123">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the title bar or icon title in its active colors when the *wParam* parameter is **TRUE** and in its inactive colors when *wParam* is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8872a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8872a-124">Requirements</span></span>



| <span data-ttu-id="8872a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8872a-125">Requirement</span></span> | <span data-ttu-id="8872a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8872a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8872a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8872a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8872a-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8872a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8872a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8872a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8872a-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8872a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8872a-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8872a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8872a-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8872a-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8872a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8872a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="8872a-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8872a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8872a-135">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8872a-135">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="8872a-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8872a-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8872a-137">Windows</span><span class="sxs-lookup"><span data-stu-id="8872a-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
