---
description: Il \_ messaggio WM SYSCOLORCHANGE viene inviato a tutte le finestre di primo livello quando viene apportata una modifica a un'impostazione dei colori di sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Messaggio WM_SYSCOLORCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980791"
---
# <a name="wm_syscolorchange-message"></a><span data-ttu-id="0cb05-103">\_Messaggio SYSCOLORCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="0cb05-103">WM\_SYSCOLORCHANGE message</span></span>

<span data-ttu-id="0cb05-104">Il messaggio **WM \_ SYSCOLORCHANGE** viene inviato a tutte le finestre di primo livello quando viene apportata una modifica a un'impostazione dei colori di sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb05-104">The **WM\_SYSCOLORCHANGE** message is sent to all top-level windows when a change is made to a system color setting.</span></span>

<span data-ttu-id="0cb05-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0cb05-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="0cb05-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cb05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cb05-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cb05-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="0cb05-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0cb05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cb05-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cb05-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="0cb05-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cb05-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cb05-111">Remarks</span></span>

<span data-ttu-id="0cb05-112">Il sistema invia un messaggio di [**\_ disegno WM**](wm-paint.md) a qualsiasi finestra interessata da una modifica del colore di sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb05-112">The system sends a [**WM\_PAINT**](wm-paint.md) message to any window that is affected by a system color change.</span></span>

<span data-ttu-id="0cb05-113">Le applicazioni che hanno pennelli che usano i colori di sistema esistenti devono eliminare tali pennelli e ricrearli usando i nuovi colori di sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb05-113">Applications that have brushes using the existing system colors should delete those brushes and re-create them using the new system colors.</span></span>

<span data-ttu-id="0cb05-114">Le finestre di primo livello che usano controlli comuni devono trasmettere il messaggio **WM \_ SYSCOLORCHANGE** ai controlli; in caso contrario, i controlli non riceveranno una notifica della modifica del colore.</span><span class="sxs-lookup"><span data-stu-id="0cb05-114">Top level windows that use common controls must forward the **WM\_SYSCOLORCHANGE** message to the controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="0cb05-115">In questo modo si garantisce che i colori utilizzati dai controlli comuni siano coerenti con quelli utilizzati da altri oggetti dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0cb05-115">This ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="0cb05-116">Ad esempio, un controllo Toolbar usa il colore "oggetti 3D" per creare i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0cb05-116">For example, a toolbar control uses the "3D Objects" color to draw its buttons.</span></span> <span data-ttu-id="0cb05-117">Se l'utente modifica il colore degli oggetti 3D ma il messaggio **WM \_ SYSCOLORCHANGE** non viene trasmesso alla barra degli strumenti, i pulsanti della barra degli strumenti rimarranno nel colore originale mentre viene modificato il colore di altri pulsanti del sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb05-117">If the user changes the 3D Objects color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color while the color of other buttons in the system changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb05-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cb05-118">Requirements</span></span>



| <span data-ttu-id="0cb05-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb05-119">Requirement</span></span> | <span data-ttu-id="0cb05-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0cb05-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb05-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb05-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb05-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cb05-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0cb05-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb05-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb05-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cb05-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0cb05-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cb05-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb05-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0cb05-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb05-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cb05-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb05-128">Panoramica sui colori</span><span class="sxs-lookup"><span data-stu-id="0cb05-128">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="0cb05-129">Messaggi colori</span><span class="sxs-lookup"><span data-stu-id="0cb05-129">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="0cb05-130">**\_disegno WM**</span><span class="sxs-lookup"><span data-stu-id="0cb05-130">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
