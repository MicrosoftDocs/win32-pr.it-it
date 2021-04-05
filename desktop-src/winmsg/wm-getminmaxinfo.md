---
description: Inviato a una finestra quando la dimensione o la posizione della finestra sta per essere modificata. Un'applicazione può utilizzare questo messaggio per eseguire l'override delle dimensioni e della posizione ingrandite predefinite della finestra o della dimensione minima o massima predefinita del rilevamento.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Messaggio WM_GETMINMAXINFO (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883402"
---
# <a name="wm_getminmaxinfo-message"></a><span data-ttu-id="b450b-104">\_Messaggio GETMINMAXINFO WM</span><span class="sxs-lookup"><span data-stu-id="b450b-104">WM\_GETMINMAXINFO message</span></span>

<span data-ttu-id="b450b-105">Inviato a una finestra quando la dimensione o la posizione della finestra sta per essere modificata.</span><span class="sxs-lookup"><span data-stu-id="b450b-105">Sent to a window when the size or position of the window is about to change.</span></span> <span data-ttu-id="b450b-106">Un'applicazione può utilizzare questo messaggio per eseguire l'override delle dimensioni e della posizione ingrandite predefinite della finestra o della dimensione minima o massima predefinita del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="b450b-106">An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.</span></span>

<span data-ttu-id="b450b-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b450b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a><span data-ttu-id="b450b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b450b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b450b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b450b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b450b-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="b450b-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b450b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b450b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b450b-112">Puntatore a una struttura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) che contiene la posizione e le dimensioni ingrandite predefinite e le dimensioni minime e massime predefinite del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="b450b-112">A pointer to a [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes.</span></span> <span data-ttu-id="b450b-113">Un'applicazione può eseguire l'override delle impostazioni predefinite impostando i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="b450b-113">An application can override the defaults by setting the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b450b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b450b-114">Return value</span></span>

<span data-ttu-id="b450b-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b450b-115">Type: **LRESULT**</span></span>

<span data-ttu-id="b450b-116">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="b450b-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b450b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b450b-117">Remarks</span></span>

<span data-ttu-id="b450b-118">La dimensione massima del rilevamento è la dimensione della finestra più grande che può essere prodotta usando i bordi per ridimensionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="b450b-118">The maximum tracking size is the largest window size that can be produced by using the borders to size the window.</span></span> <span data-ttu-id="b450b-119">La dimensione minima del rilevamento è la dimensione minima della finestra che può essere prodotta usando i bordi per ridimensionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="b450b-119">The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b450b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b450b-120">Requirements</span></span>



| <span data-ttu-id="b450b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b450b-121">Requirement</span></span> | <span data-ttu-id="b450b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b450b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b450b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b450b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b450b-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b450b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b450b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b450b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b450b-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b450b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b450b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b450b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b450b-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b450b-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b450b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b450b-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b450b-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b450b-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b450b-131">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="b450b-131">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="b450b-132">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="b450b-132">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="b450b-133">**MINMAXINFO**</span><span class="sxs-lookup"><span data-stu-id="b450b-133">**MINMAXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

<span data-ttu-id="b450b-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b450b-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b450b-135">Windows</span><span class="sxs-lookup"><span data-stu-id="b450b-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
