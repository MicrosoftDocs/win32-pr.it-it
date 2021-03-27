---
description: Il \_ messaggio WM PALETTECHANGED viene inviato a tutte le finestre di primo livello e sovrapposte dopo che la finestra con lo stato attivo della tastiera ha realizzato la relativa tavolozza logica, modificando quindi la tavolozza di sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Messaggio WM_PALETTECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755823"
---
# <a name="wm_palettechanged-message"></a><span data-ttu-id="d21b2-103">\_Messaggio PALETTECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="d21b2-103">WM\_PALETTECHANGED message</span></span>

<span data-ttu-id="d21b2-104">Il messaggio **WM \_ PALETTECHANGED** viene inviato a tutte le finestre di primo livello e sovrapposte dopo che la finestra con lo stato attivo della tastiera ha realizzato la relativa tavolozza logica, modificando quindi la tavolozza di sistema.</span><span class="sxs-lookup"><span data-stu-id="d21b2-104">The **WM\_PALETTECHANGED** message is sent to all top-level and overlapped windows after the window with the keyboard focus has realized its logical palette, thereby changing the system palette.</span></span> <span data-ttu-id="d21b2-105">Questo messaggio consente a una finestra che utilizza una tavolozza dei colori ma non ha lo stato attivo per realizzare la tavolozza logica e aggiornare la relativa area client.</span><span class="sxs-lookup"><span data-stu-id="d21b2-105">This message enables a window that uses a color palette but does not have the keyboard focus to realize its logical palette and update its client area.</span></span>

<span data-ttu-id="d21b2-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d21b2-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="d21b2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d21b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d21b2-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d21b2-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d21b2-109">Handle per la finestra che ha causato la modifica della tavolozza di sistema.</span><span class="sxs-lookup"><span data-stu-id="d21b2-109">A handle to the window that caused the system palette to change.</span></span>

</dd> <dt>

<span data-ttu-id="d21b2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d21b2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d21b2-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="d21b2-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d21b2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d21b2-112">Remarks</span></span>

<span data-ttu-id="d21b2-113">Questo messaggio deve essere inviato a tutte le finestre di primo livello e sovrapposte, incluso quello che ha modificato la tavolozza di sistema.</span><span class="sxs-lookup"><span data-stu-id="d21b2-113">This message must be sent to all top-level and overlapped windows, including the one that changed the system palette.</span></span> <span data-ttu-id="d21b2-114">Se le finestre figlio utilizzano una tavolozza dei colori, è necessario passare anche questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d21b2-114">If any child windows use a color palette, this message must be passed on to them as well.</span></span>

<span data-ttu-id="d21b2-115">Per evitare la creazione di un ciclo infinito, una finestra che riceve questo messaggio non deve realizzare la propria tavolozza, a meno che il *wParam* non contenga il proprio handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="d21b2-115">To avoid creating an infinite loop, a window that receives this message must not realize its palette, unless it determines that *wParam* does not contain its own window handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="d21b2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d21b2-116">Requirements</span></span>



| <span data-ttu-id="d21b2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d21b2-117">Requirement</span></span> | <span data-ttu-id="d21b2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d21b2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d21b2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d21b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d21b2-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d21b2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d21b2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d21b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d21b2-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d21b2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d21b2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d21b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d21b2-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d21b2-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d21b2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d21b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d21b2-126">Panoramica sui colori</span><span class="sxs-lookup"><span data-stu-id="d21b2-126">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="d21b2-127">Messaggi colori</span><span class="sxs-lookup"><span data-stu-id="d21b2-127">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="d21b2-128">**\_PALETTEISCHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="d21b2-128">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> <dt>

[<span data-ttu-id="d21b2-129">**\_QUERYNEWPALETTE WM**</span><span class="sxs-lookup"><span data-stu-id="d21b2-129">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
