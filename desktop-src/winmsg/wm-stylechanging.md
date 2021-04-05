---
description: Inviato a una finestra quando la funzione SetWindowLong sta per modificare uno o più stili della finestra.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Messaggio WM_STYLECHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881878"
---
# <a name="wm_stylechanging-message"></a><span data-ttu-id="207ea-103">\_Messaggio STYLECHANGING WM</span><span class="sxs-lookup"><span data-stu-id="207ea-103">WM\_STYLECHANGING message</span></span>

<span data-ttu-id="207ea-104">Inviato a una finestra quando la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) sta per modificare uno o più stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="207ea-104">Sent to a window when the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is about to change one or more of the window's styles.</span></span>

<span data-ttu-id="207ea-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="207ea-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a><span data-ttu-id="207ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="207ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="207ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="207ea-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="207ea-108">Indica se gli stili della finestra o gli stili estesi della finestra sono in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="207ea-108">Indicates whether the window's styles or extended window styles are changing.</span></span> <span data-ttu-id="207ea-109">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="207ea-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="207ea-110">Valore</span><span class="sxs-lookup"><span data-stu-id="207ea-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="207ea-111">Significato</span><span class="sxs-lookup"><span data-stu-id="207ea-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="207ea-112"><dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="207ea-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="207ea-113">Gli stili estesi della finestra sono in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="207ea-113">The extended window styles are changing.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="207ea-114"><dt>**GWL \_ STILE**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="207ea-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="207ea-115">Gli stili della finestra sono in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="207ea-115">The window styles are changing.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="207ea-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="207ea-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="207ea-117">Puntatore a una struttura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) che contiene i nuovi stili proposti per la finestra.</span><span class="sxs-lookup"><span data-stu-id="207ea-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the proposed new styles for the window.</span></span> <span data-ttu-id="207ea-118">Un'applicazione può esaminare gli stili e, se necessario, modificarli.</span><span class="sxs-lookup"><span data-stu-id="207ea-118">An application can examine the styles and, if necessary, change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="207ea-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="207ea-119">Return value</span></span>

<span data-ttu-id="207ea-120">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="207ea-120">Type: **LRESULT**</span></span>

<span data-ttu-id="207ea-121">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="207ea-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="207ea-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="207ea-122">Requirements</span></span>



| <span data-ttu-id="207ea-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="207ea-123">Requirement</span></span> | <span data-ttu-id="207ea-124">Valore</span><span class="sxs-lookup"><span data-stu-id="207ea-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="207ea-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="207ea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="207ea-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="207ea-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="207ea-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="207ea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="207ea-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="207ea-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="207ea-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="207ea-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="207ea-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="207ea-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="207ea-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="207ea-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="207ea-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="207ea-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="207ea-133">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="207ea-133">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="207ea-134">**\_STYLECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="207ea-134">**WM\_STYLECHANGED**</span></span>](wm-stylechanged.md)
</dt> <dt>

<span data-ttu-id="207ea-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="207ea-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="207ea-136">Windows</span><span class="sxs-lookup"><span data-stu-id="207ea-136">Windows</span></span>](windows.md)
</dt> </dl>

 

 
