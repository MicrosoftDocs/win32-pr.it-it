---
description: Associa una nuova icona grande o piccola a una finestra. Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Messaggio WM_SETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231544"
---
# <a name="wm_seticon-message"></a><span data-ttu-id="2bd7a-104">\_Messaggio dell'icona WM</span><span class="sxs-lookup"><span data-stu-id="2bd7a-104">WM\_SETICON message</span></span>

<span data-ttu-id="2bd7a-105">Associa una nuova icona grande o piccola a una finestra.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-105">Associates a new large or small icon with a window.</span></span> <span data-ttu-id="2bd7a-106">Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-106">The system displays the large icon in the ALT+TAB dialog box, and the small icon in the window caption.</span></span>


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a><span data-ttu-id="2bd7a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2bd7a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd7a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bd7a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd7a-109">Tipo di icona da impostare.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-109">The type of icon to be set.</span></span> <span data-ttu-id="2bd7a-110">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2bd7a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd7a-111">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="2bd7a-112">Significato</span><span class="sxs-lookup"><span data-stu-id="2bd7a-112">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="2bd7a-113"><dt>**Icona \_ di BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2bd7a-113"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="2bd7a-114">Impostare l'icona grande per la finestra.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-114">Set the large icon for the window.</span></span><br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="2bd7a-115"><dt>**Icona \_ di PICCOLO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2bd7a-115"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="2bd7a-116">Impostare l'icona piccola per la finestra.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-116">Set the small icon for the window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2bd7a-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bd7a-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd7a-118">Handle per la nuova icona grande o piccola.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-118">A handle to the new large or small icon.</span></span> <span data-ttu-id="2bd7a-119">Se questo parametro è **null**, l'icona indicata da *wParam* viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-119">If this parameter is **NULL**, the icon indicated by *wParam* is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bd7a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2bd7a-120">Return value</span></span>

<span data-ttu-id="2bd7a-121">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2bd7a-121">Type: **LRESULT**</span></span>

<span data-ttu-id="2bd7a-122">Il valore restituito è un handle per l'icona grande o piccola precedente, a seconda del valore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-122">The return value is a handle to the previous large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="2bd7a-123">È **null** se la finestra in precedenza non aveva alcuna icona del tipo indicato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-123">It is **NULL** if the window previously had no icon of the type indicated by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd7a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bd7a-124">Remarks</span></span>

<span data-ttu-id="2bd7a-125">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce un handle per l'icona grande o piccola precedente associata alla finestra, a seconda del valore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="2bd7a-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns a handle to the previous large or small icon associated with the window, depending on the value of *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd7a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bd7a-126">Requirements</span></span>



| <span data-ttu-id="2bd7a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd7a-127">Requirement</span></span> | <span data-ttu-id="2bd7a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd7a-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd7a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd7a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd7a-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bd7a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2bd7a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd7a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd7a-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bd7a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2bd7a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bd7a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd7a-134"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bd7a-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd7a-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bd7a-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bd7a-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2bd7a-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2bd7a-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2bd7a-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2bd7a-138">**\_icona WM GETicon**</span><span class="sxs-lookup"><span data-stu-id="2bd7a-138">**WM\_GETICON**</span></span>](wm-geticon.md)
</dt> <dt>

<span data-ttu-id="2bd7a-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2bd7a-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2bd7a-140">Windows</span><span class="sxs-lookup"><span data-stu-id="2bd7a-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
