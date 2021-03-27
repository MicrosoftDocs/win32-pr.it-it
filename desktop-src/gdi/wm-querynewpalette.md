---
description: Il \_ messaggio WM QUERYNEWPALETTE informa una finestra che sta per ricevere lo stato attivo della tastiera, offrendo alla finestra la possibilità di realizzare la propria tavolozza logica quando riceve lo stato attivo.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Messaggio WM_QUERYNEWPALETTE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979354"
---
# <a name="wm_querynewpalette-message"></a><span data-ttu-id="62142-103">\_Messaggio QUERYNEWPALETTE WM</span><span class="sxs-lookup"><span data-stu-id="62142-103">WM\_QUERYNEWPALETTE message</span></span>

<span data-ttu-id="62142-104">Il messaggio **WM \_ QUERYNEWPALETTE** informa una finestra che sta per ricevere lo stato attivo della tastiera, offrendo alla finestra la possibilità di realizzare la propria tavolozza logica quando riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="62142-104">The **WM\_QUERYNEWPALETTE** message informs a window that it is about to receive the keyboard focus, giving the window the opportunity to realize its logical palette when it receives the focus.</span></span>

<span data-ttu-id="62142-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="62142-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="62142-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62142-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62142-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62142-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="62142-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62142-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62142-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62142-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="62142-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62142-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62142-111">Return value</span></span>

<span data-ttu-id="62142-112">Se la finestra comprende la tavolozza logica, deve restituire **true**; in caso contrario, deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="62142-112">If the window realizes its logical palette, it must return **TRUE**; otherwise, it must return **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62142-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62142-113">Requirements</span></span>



| <span data-ttu-id="62142-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="62142-114">Requirement</span></span> | <span data-ttu-id="62142-115">Valore</span><span class="sxs-lookup"><span data-stu-id="62142-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62142-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62142-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62142-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62142-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="62142-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62142-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62142-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62142-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62142-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62142-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62142-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62142-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62142-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62142-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62142-123">Panoramica sui colori</span><span class="sxs-lookup"><span data-stu-id="62142-123">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="62142-124">Messaggi colori</span><span class="sxs-lookup"><span data-stu-id="62142-124">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="62142-125">**\_PALETTECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="62142-125">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="62142-126">**\_PALETTEISCHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="62142-126">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> </dl>

 

 
