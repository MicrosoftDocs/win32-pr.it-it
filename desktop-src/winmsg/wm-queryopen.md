---
description: Inviato a un'icona quando l'utente richiede che la finestra venga ripristinata alle dimensioni e alla posizione precedenti.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Messaggio WM_QUERYOPEN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050035"
---
# <a name="wm_queryopen-message"></a><span data-ttu-id="6e898-103">\_Messaggio QUERYOPEN WM</span><span class="sxs-lookup"><span data-stu-id="6e898-103">WM\_QUERYOPEN message</span></span>

<span data-ttu-id="6e898-104">Inviato a un'icona quando l'utente richiede che la finestra venga ripristinata alle dimensioni e alla posizione precedenti.</span><span class="sxs-lookup"><span data-stu-id="6e898-104">Sent to an icon when the user requests that the window be restored to its previous size and position.</span></span>

<span data-ttu-id="6e898-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6e898-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a><span data-ttu-id="6e898-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e898-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e898-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e898-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e898-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="6e898-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e898-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e898-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e898-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="6e898-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e898-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e898-111">Return value</span></span>

<span data-ttu-id="6e898-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6e898-112">Type: **LRESULT**</span></span>

<span data-ttu-id="6e898-113">Se è possibile aprire l'icona, un'applicazione che elabora questo messaggio deve restituire **true**. in caso contrario, deve restituire **false** per impedire l'apertura dell'icona.</span><span class="sxs-lookup"><span data-stu-id="6e898-113">If the icon can be opened, an application that processes this message should return **TRUE**; otherwise, it should return **FALSE** to prevent the icon from being opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e898-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e898-114">Remarks</span></span>

<span data-ttu-id="6e898-115">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="6e898-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE**.</span></span>

<span data-ttu-id="6e898-116">Durante l'elaborazione di questo messaggio, l'applicazione non deve eseguire alcuna azione che comporterebbe una modifica dell'attivazione o dello stato attivo (ad esempio, la creazione di una finestra di dialogo).</span><span class="sxs-lookup"><span data-stu-id="6e898-116">While processing this message, the application should not perform any action that would cause an activation or focus change (for example, creating a dialog box).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e898-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e898-117">Requirements</span></span>



| <span data-ttu-id="6e898-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e898-118">Requirement</span></span> | <span data-ttu-id="6e898-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6e898-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e898-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e898-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e898-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e898-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e898-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e898-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e898-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e898-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e898-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e898-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e898-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e898-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e898-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e898-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e898-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6e898-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6e898-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6e898-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="6e898-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6e898-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6e898-130">Windows</span><span class="sxs-lookup"><span data-stu-id="6e898-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
