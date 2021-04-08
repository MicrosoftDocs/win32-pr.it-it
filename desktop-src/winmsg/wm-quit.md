---
description: Indica una richiesta di terminazione di un'applicazione e viene generata quando l'applicazione chiama la funzione PostQuitMessage. Questo messaggio causa la restituzione di zero da parte della funzione GetMessage.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Messaggio WM_QUIT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050045"
---
# <a name="wm_quit-message"></a><span data-ttu-id="e7766-104">\_Messaggio WM Quit</span><span class="sxs-lookup"><span data-stu-id="e7766-104">WM\_QUIT message</span></span>

<span data-ttu-id="e7766-105">Indica una richiesta di terminazione di un'applicazione e viene generata quando l'applicazione chiama la funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="e7766-105">Indicates a request to terminate an application, and is generated when the application calls the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span> <span data-ttu-id="e7766-106">Questo messaggio causa la restituzione di zero da parte della funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) .</span><span class="sxs-lookup"><span data-stu-id="e7766-106">This message causes the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function to return zero.</span></span>


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a><span data-ttu-id="e7766-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7766-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7766-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7766-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7766-109">Codice di uscita specificato nella funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="e7766-109">The exit code given in the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="e7766-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7766-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7766-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="e7766-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7766-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7766-112">Return value</span></span>

<span data-ttu-id="e7766-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7766-113">Type: **LRESULT**</span></span>

<span data-ttu-id="e7766-114">Questo messaggio non ha un valore restituito perché causa l'interruzione del ciclo di messaggi prima che il messaggio venga inviato alla routine della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7766-114">This message does not have a return value because it causes the message loop to terminate before the message is sent to the application's window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7766-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7766-115">Remarks</span></span>

<span data-ttu-id="e7766-116">Il messaggio **WM \_ Quit** non è associato a una finestra e pertanto non verrà mai ricevuto tramite la procedura finestra di una finestra.</span><span class="sxs-lookup"><span data-stu-id="e7766-116">The **WM\_QUIT** message is not associated with a window and therefore will never be received through a window's window procedure.</span></span> <span data-ttu-id="e7766-117">Viene recuperato solo dalle funzioni [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="e7766-117">It is retrieved only by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions.</span></span>

<span data-ttu-id="e7766-118">Non pubblicare il messaggio **WM \_ Quit** usando la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; usare [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="e7766-118">Do not post the **WM\_QUIT** message using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7766-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7766-119">Requirements</span></span>



| <span data-ttu-id="e7766-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7766-120">Requirement</span></span> | <span data-ttu-id="e7766-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e7766-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7766-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7766-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7766-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7766-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e7766-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7766-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7766-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7766-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7766-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7766-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7766-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7766-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7766-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7766-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7766-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e7766-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e7766-130">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="e7766-130">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="e7766-131">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="e7766-131">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="e7766-132">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="e7766-132">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

<span data-ttu-id="e7766-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e7766-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e7766-134">Windows</span><span class="sxs-lookup"><span data-stu-id="e7766-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
