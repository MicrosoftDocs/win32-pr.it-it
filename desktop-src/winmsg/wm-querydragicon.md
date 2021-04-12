---
description: Inviato a una finestra ridotta a icona.
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Messaggio WM_QUERYDRAGICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345581"
---
# <a name="wm_querydragicon-message"></a><span data-ttu-id="e9914-103">\_Messaggio QUERYDRAGICON WM</span><span class="sxs-lookup"><span data-stu-id="e9914-103">WM\_QUERYDRAGICON message</span></span>

<span data-ttu-id="e9914-104">Inviato a una finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="e9914-104">Sent to a minimized (iconic) window.</span></span> <span data-ttu-id="e9914-105">La finestra sta per essere trascinata dall'utente, ma non dispone di un'icona definita per la relativa classe.</span><span class="sxs-lookup"><span data-stu-id="e9914-105">The window is about to be dragged by the user but does not have an icon defined for its class.</span></span> <span data-ttu-id="e9914-106">Un'applicazione può restituire un handle per un'icona o un cursore.</span><span class="sxs-lookup"><span data-stu-id="e9914-106">An application can return a handle to an icon or cursor.</span></span> <span data-ttu-id="e9914-107">Il sistema Visualizza il cursore o l'icona quando l'utente trascina l'icona.</span><span class="sxs-lookup"><span data-stu-id="e9914-107">The system displays this cursor or icon while the user drags the icon.</span></span>

<span data-ttu-id="e9914-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e9914-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a><span data-ttu-id="e9914-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9914-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9914-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9914-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9914-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="e9914-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9914-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9914-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9914-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="e9914-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9914-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9914-114">Return value</span></span>

<span data-ttu-id="e9914-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e9914-115">Type: **LRESULT**</span></span>

<span data-ttu-id="e9914-116">Un'applicazione deve restituire un handle a un cursore o a un'icona visualizzata dal sistema mentre l'utente trascina l'icona.</span><span class="sxs-lookup"><span data-stu-id="e9914-116">An application should return a handle to a cursor or icon that the system is to display while the user drags the icon.</span></span> <span data-ttu-id="e9914-117">Il cursore o l'icona deve essere compatibile con la risoluzione del driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9914-117">The cursor or icon must be compatible with the display driver's resolution.</span></span> <span data-ttu-id="e9914-118">Se l'applicazione restituisce **null**, il sistema Visualizza il cursore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e9914-118">If the application returns **NULL**, the system displays the default cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9914-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9914-119">Remarks</span></span>

<span data-ttu-id="e9914-120">Quando l'utente trascina l'icona di una finestra senza un'icona di classe, il sistema sostituisce l'icona con un cursore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e9914-120">When the user drags the icon of a window without a class icon, the system replaces the icon with a default cursor.</span></span> <span data-ttu-id="e9914-121">Se l'applicazione richiede la visualizzazione di un cursore diverso durante il trascinamento, deve restituire un handle per il cursore o l'icona compatibile con la risoluzione del driver visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e9914-121">If the application requires a different cursor to be displayed during dragging, it must return a handle to the cursor or icon compatible with the display driver's resolution.</span></span> <span data-ttu-id="e9914-122">Se un'applicazione restituisce un handle a un cursore o a un'icona di colore, il sistema converte il cursore o l'icona in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="e9914-122">If an application returns a handle to a color cursor or icon, the system converts the cursor or icon to black and white.</span></span> <span data-ttu-id="e9914-123">L'applicazione può chiamare la funzione [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) o [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) per caricare un cursore o un'icona dalle risorse nel file eseguibile (exe) e recuperare questo handle.</span><span class="sxs-lookup"><span data-stu-id="e9914-123">The application can call the [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) or [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to load a cursor or icon from the resources in its executable (.exe) file and to retrieve this handle.</span></span>

<span data-ttu-id="e9914-124">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="e9914-124">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="e9914-125">Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e9914-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9914-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9914-126">Requirements</span></span>



| <span data-ttu-id="e9914-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9914-127">Requirement</span></span> | <span data-ttu-id="e9914-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e9914-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9914-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9914-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e9914-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9914-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9914-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9914-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e9914-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9914-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9914-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9914-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9914-134"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9914-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9914-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9914-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9914-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e9914-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9914-137">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="e9914-137">**LoadCursor**</span></span>](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[<span data-ttu-id="e9914-138">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="e9914-138">**LoadIcon**</span></span>](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

<span data-ttu-id="e9914-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e9914-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9914-140">Windows</span><span class="sxs-lookup"><span data-stu-id="e9914-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
