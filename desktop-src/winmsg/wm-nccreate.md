---
description: Inviato prima del messaggio di \_ creazione di WM quando una finestra viene creata per la prima volta.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Messaggio WM_NCCREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312368"
---
# <a name="wm_nccreate-message"></a><span data-ttu-id="dc774-103">\_Messaggio NCCREATE WM</span><span class="sxs-lookup"><span data-stu-id="dc774-103">WM\_NCCREATE message</span></span>

<span data-ttu-id="dc774-104">Inviato prima del messaggio [**di \_ creazione di WM**](wm-create.md) quando una finestra viene creata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="dc774-104">Sent prior to the [**WM\_CREATE**](wm-create.md) message when a window is first created.</span></span>

<span data-ttu-id="dc774-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dc774-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a><span data-ttu-id="dc774-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc774-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc774-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc774-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc774-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="dc774-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc774-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc774-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc774-110">Puntatore alla struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) che contiene informazioni sulla finestra da creare.</span><span class="sxs-lookup"><span data-stu-id="dc774-110">A pointer to the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span> <span data-ttu-id="dc774-111">I membri di **struttura CREATESTRUCT** sono identici ai parametri della funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="dc774-111">The members of **CREATESTRUCT** are identical to the parameters of the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc774-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc774-112">Return value</span></span>

<span data-ttu-id="dc774-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc774-113">Type: **LRESULT**</span></span>

<span data-ttu-id="dc774-114">Se un'applicazione elabora il messaggio, deve restituire **true** per continuare la creazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="dc774-114">If an application processes this message, it should return **TRUE** to continue creation of the window.</span></span> <span data-ttu-id="dc774-115">Se l'applicazione restituisce **false**, la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) restituirà un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="dc774-115">If the application returns **FALSE**, the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function will return a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc774-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc774-116">Requirements</span></span>



| <span data-ttu-id="dc774-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc774-117">Requirement</span></span> | <span data-ttu-id="dc774-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dc774-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc774-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc774-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dc774-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc774-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dc774-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc774-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dc774-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc774-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc774-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc774-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc774-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc774-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc774-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc774-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc774-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="dc774-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dc774-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="dc774-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="dc774-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="dc774-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="dc774-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dc774-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="dc774-130">**STRUTTURA CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="dc774-130">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="dc774-131">**creazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="dc774-131">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

<span data-ttu-id="dc774-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="dc774-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dc774-133">Windows</span><span class="sxs-lookup"><span data-stu-id="dc774-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
