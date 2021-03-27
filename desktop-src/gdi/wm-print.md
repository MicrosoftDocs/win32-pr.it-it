---
description: Il \_ messaggio di stampa WM viene inviato a una finestra per richiedere che venga disegnato nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Messaggio WM_PRINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049873"
---
# <a name="wm_print-message"></a><span data-ttu-id="8d1fc-103">\_Messaggio di stampa WM</span><span class="sxs-lookup"><span data-stu-id="8d1fc-103">WM\_PRINT message</span></span>

<span data-ttu-id="8d1fc-104">Il messaggio di **\_ stampa WM** viene inviato a una finestra per richiedere che venga disegnato nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-104">The **WM\_PRINT** message is sent to a window to request that it draw itself in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="8d1fc-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d1fc-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="8d1fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d1fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d1fc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d1fc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d1fc-108">Handle per il contesto di dispositivo da creare.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-108">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="8d1fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d1fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d1fc-110">Opzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-110">The drawing options.</span></span> <span data-ttu-id="8d1fc-111">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8d1fc-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8d1fc-112">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="8d1fc-113">Significato</span><span class="sxs-lookup"><span data-stu-id="8d1fc-113">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="8d1fc-114"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="8d1fc-114"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="8d1fc-115">Disegna la finestra solo se è visibile.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-115">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="8d1fc-116"><dt>**\_elementi figlio PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="8d1fc-116"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="8d1fc-117">Disegna tutte le finestre figlio visibili.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-117">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="8d1fc-118"><dt>**\_client PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="8d1fc-118"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="8d1fc-119">Disegna l'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-119">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="8d1fc-120"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="8d1fc-120"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="8d1fc-121">Cancella lo sfondo prima di disegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-121">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="8d1fc-122"><dt>**non \_ client PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="8d1fc-122"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="8d1fc-123">Disegna l'area non client della finestra.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-123">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="8d1fc-124"><dt>**\_Proprietà PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="8d1fc-124"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="8d1fc-125">Disegna tutte le finestre di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d1fc-125">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d1fc-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d1fc-126">Remarks</span></span>

<span data-ttu-id="8d1fc-127">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora questo messaggio in base all'opzione di disegno specificata: se si \_ specifica PRF CHECKVISIBLE e la finestra non è visibile, non eseguire alcuna operazione se \_ si specifica PRF non client, creare l'area non client nel contesto di dispositivo specificato. Se \_ si specifica PRF ERASEBKGND, inviare alla finestra un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , se \_ è specificato il client PRF, inviare alla finestra un messaggio [**WM \_ PRINTCLIENT**](wm-printclient.md) , se \_ è impostato PRF Children, inviare ogni finestra figlio visibile un messaggio di **\_ stampa WM** , se \_ è impostata la proprietà PRF, inviare ogni finestra di proprietà visibile a un messaggio di **\_ stampa WM** .</span><span class="sxs-lookup"><span data-stu-id="8d1fc-127">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes this message based on which drawing option is specified: if PRF\_CHECKVISIBLE is specified and the window is not visible, do nothing, if PRF\_NONCLIENT is specified, draw the nonclient area in the specified device context, if PRF\_ERASEBKGND is specified, send the window a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message, if PRF\_CLIENT is specified, send the window a [**WM\_PRINTCLIENT**](wm-printclient.md) message, if PRF\_CHILDREN is set, send each visible child window a **WM\_PRINT** message, if PRF\_OWNED is set, send each visible owned window a **WM\_PRINT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1fc-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d1fc-128">Requirements</span></span>



| <span data-ttu-id="8d1fc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d1fc-129">Requirement</span></span> | <span data-ttu-id="8d1fc-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8d1fc-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1fc-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d1fc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8d1fc-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8d1fc-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8d1fc-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d1fc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8d1fc-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8d1fc-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d1fc-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d1fc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d1fc-136"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d1fc-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d1fc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d1fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1fc-138">Cenni preliminari su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="8d1fc-138">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="8d1fc-139">Disegno e creazione di messaggi</span><span class="sxs-lookup"><span data-stu-id="8d1fc-139">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="8d1fc-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8d1fc-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8d1fc-141">**\_ERASEBKGND WM**</span><span class="sxs-lookup"><span data-stu-id="8d1fc-141">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="8d1fc-142">**\_PRINTCLIENT WM**</span><span class="sxs-lookup"><span data-stu-id="8d1fc-142">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
