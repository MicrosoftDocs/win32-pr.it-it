---
description: Inviato quando un'applicazione richiede la creazione di una finestra chiamando la funzione CreateWindowEx o CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Messaggio WM_CREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314871"
---
# <a name="wm_create-message"></a><span data-ttu-id="eb80f-103">\_Creazione messaggio WM</span><span class="sxs-lookup"><span data-stu-id="eb80f-103">WM\_CREATE message</span></span>

<span data-ttu-id="eb80f-104">Inviato quando un'applicazione richiede la creazione di una finestra chiamando la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="eb80f-104">Sent when an application requests that a window be created by calling the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="eb80f-105">Il messaggio viene inviato prima che la funzione restituisca. La routine della finestra della nuova finestra riceve questo messaggio dopo la creazione della finestra, ma prima che la finestra diventi visibile.</span><span class="sxs-lookup"><span data-stu-id="eb80f-105">(The message is sent before the function returns.) The window procedure of the new window receives this message after the window is created, but before the window becomes visible.</span></span>

<span data-ttu-id="eb80f-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="eb80f-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a><span data-ttu-id="eb80f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb80f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb80f-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb80f-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb80f-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="eb80f-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb80f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb80f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb80f-111">Puntatore a una struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) contenente informazioni sulla finestra da creare.</span><span class="sxs-lookup"><span data-stu-id="eb80f-111">A pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb80f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb80f-112">Return value</span></span>

<span data-ttu-id="eb80f-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="eb80f-113">Type: **LRESULT**</span></span>

<span data-ttu-id="eb80f-114">Se un'applicazione elabora il messaggio, deve restituire zero per continuare la creazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="eb80f-114">If an application processes this message, it should return zero to continue creation of the window.</span></span> <span data-ttu-id="eb80f-115">Se l'applicazione restituisce-1, la finestra viene distrutta e la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) restituisce un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="eb80f-115">If the application returns –1, the window is destroyed and the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function returns a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb80f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb80f-116">Requirements</span></span>



| <span data-ttu-id="eb80f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb80f-117">Requirement</span></span> | <span data-ttu-id="eb80f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="eb80f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb80f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb80f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb80f-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eb80f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eb80f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb80f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb80f-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eb80f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb80f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb80f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb80f-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb80f-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb80f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb80f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb80f-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="eb80f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eb80f-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="eb80f-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="eb80f-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="eb80f-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="eb80f-129">**STRUTTURA CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="eb80f-129">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="eb80f-130">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="eb80f-130">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="eb80f-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="eb80f-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eb80f-132">Windows</span><span class="sxs-lookup"><span data-stu-id="eb80f-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
