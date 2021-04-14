---
title: Messaggio WM_SETFOCUS (winuser. h)
description: Inviato a una finestra dopo che ha ottenuto lo stato attivo della tastiera.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- Input della tastiera e del mouse WM_SETFOCUS messaggio
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478760"
---
# <a name="wm_setfocus-message"></a><span data-ttu-id="5f026-104">Messaggio di SetFocus di WM \_</span><span class="sxs-lookup"><span data-stu-id="5f026-104">WM\_SETFOCUS message</span></span>

<span data-ttu-id="5f026-105">Inviato a una finestra dopo che ha ottenuto lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="5f026-105">Sent to a window after it has gained the keyboard focus.</span></span>


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a><span data-ttu-id="5f026-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f026-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f026-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f026-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f026-108">Handle per la finestra che ha perso lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="5f026-108">A handle to the window that has lost the keyboard focus.</span></span> <span data-ttu-id="5f026-109">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5f026-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5f026-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f026-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f026-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5f026-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f026-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f026-112">Return value</span></span>

<span data-ttu-id="5f026-113">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="5f026-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f026-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f026-114">Remarks</span></span>

<span data-ttu-id="5f026-115">Per visualizzare un accento circonflesso, un'applicazione deve chiamare le funzioni del cursore appropriate quando riceve il messaggio **di \_ SetFocus di WM** .</span><span class="sxs-lookup"><span data-stu-id="5f026-115">To display a caret, an application should call the appropriate caret functions when it receives the **WM\_SETFOCUS** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f026-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f026-116">Requirements</span></span>



| <span data-ttu-id="5f026-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f026-117">Requirement</span></span> | <span data-ttu-id="5f026-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5f026-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f026-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f026-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f026-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f026-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5f026-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f026-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f026-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f026-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f026-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f026-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f026-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f026-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f026-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f026-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f026-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5f026-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f026-127">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="5f026-127">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="5f026-128">**\_KILLFOCUS WM**</span><span class="sxs-lookup"><span data-stu-id="5f026-128">**WM\_KILLFOCUS**</span></span>](wm-killfocus.md)
</dt> <dt>

<span data-ttu-id="5f026-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5f026-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f026-130">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="5f026-130">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

