---
description: Un'applicazione invia il \_ messaggio WM SETREDRAW a una finestra per consentire il ritracciamento delle modifiche in tale finestra o per impedire che le modifiche apportate alla finestra vengano ridisegnato.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Messaggio WM_SETREDRAW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232543"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="a0bef-103">\_Messaggio SETREDRAW WM</span><span class="sxs-lookup"><span data-stu-id="a0bef-103">WM\_SETREDRAW message</span></span>

<span data-ttu-id="a0bef-104">Un'applicazione invia il messaggio **WM \_ SETREDRAW** a una finestra per consentire il ritracciamento delle modifiche in tale finestra o per impedire che le modifiche apportate alla finestra vengano ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="a0bef-104">An application sends the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="a0bef-105">Per inviare questo messaggio, chiamare la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0bef-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="a0bef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0bef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0bef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0bef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0bef-108">Stato di riestrazione.</span><span class="sxs-lookup"><span data-stu-id="a0bef-108">The redraw state.</span></span> <span data-ttu-id="a0bef-109">Se questo parametro è **true**, il contenuto può essere ridisegnato dopo una modifica.</span><span class="sxs-lookup"><span data-stu-id="a0bef-109">If this parameter is **TRUE**, the content can be redrawn after a change.</span></span> <span data-ttu-id="a0bef-110">Se questo parametro è **false**, il contenuto non può essere ridisegnato dopo una modifica.</span><span class="sxs-lookup"><span data-stu-id="a0bef-110">If this parameter is **FALSE**, the content cannot be redrawn after a change.</span></span>

</dd> <dt>

<span data-ttu-id="a0bef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0bef-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0bef-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a0bef-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0bef-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0bef-113">Return value</span></span>

<span data-ttu-id="a0bef-114">Un'applicazione restituisce zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a0bef-114">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0bef-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0bef-115">Remarks</span></span>

<span data-ttu-id="a0bef-116">Questo messaggio può essere utile se un'applicazione deve aggiungere diversi elementi a una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="a0bef-116">This message can be useful if an application must add several items to a list box.</span></span> <span data-ttu-id="a0bef-117">L'applicazione può chiamare questo messaggio con *wParam* impostato su **false**, aggiungere gli elementi, quindi chiamare di nuovo il messaggio con *wParam* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="a0bef-117">The application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="a0bef-118">Infine, l'applicazione può chiamare [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, RDW \_ Erase \| RDW \_ frame \| RDW \_ Invalidate \| RDW ALLCHILDREN \_ ) per fare in modo che la casella di riepilogo venga ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="a0bef-118">Finally, the application can call [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!Note]  
> <span data-ttu-id="a0bef-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con i flag specificati viene usato al posto di [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , perché il primo è necessario per alcuni controlli che hanno un'area non client autonomamente o con stili di finestra che ne determinano l'uso di un'area non client, ad esempio **WS \_ THICKFRAME**, **WS \_ Border** o **WS \_ ex \_ CLIENTEDGE**.</span><span class="sxs-lookup"><span data-stu-id="a0bef-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the specified flags is used instead of [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) because the former is necessary for some controls that have nonclient area on their own, or have window styles that cause them to be given a nonclient area (such as **WS\_THICKFRAME**, **WS\_BORDER**, or **WS\_EX\_CLIENTEDGE**).</span></span> <span data-ttu-id="a0bef-120">Se il controllo non dispone di un'area non client, **RedrawWindow** con questi flag eseguirà solo la maggior parte dell'invalidamento di **InvalidateRect** .</span><span class="sxs-lookup"><span data-stu-id="a0bef-120">If the control does not have a nonclient area, **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

 

<span data-ttu-id="a0bef-121">Se l'applicazione invia il messaggio **WM \_ SETREDRAW** a una finestra nascosta, la finestra diventa visibile (ovvero, il sistema operativo aggiunge lo stile **\_ visibile WS** alla finestra).</span><span class="sxs-lookup"><span data-stu-id="a0bef-121">If the application sends the **WM\_SETREDRAW** message to a hidden window, the window becomes visible (that is, the operating system adds the **WS\_VISIBLE** style to the window).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0bef-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0bef-122">Requirements</span></span>



| <span data-ttu-id="a0bef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0bef-123">Requirement</span></span> | <span data-ttu-id="a0bef-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a0bef-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bef-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0bef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bef-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0bef-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a0bef-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0bef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a0bef-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0bef-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0bef-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0bef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0bef-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0bef-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0bef-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0bef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bef-132">Cenni preliminari su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="a0bef-132">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="a0bef-133">Disegno e creazione di messaggi</span><span class="sxs-lookup"><span data-stu-id="a0bef-133">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="a0bef-134">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="a0bef-134">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
