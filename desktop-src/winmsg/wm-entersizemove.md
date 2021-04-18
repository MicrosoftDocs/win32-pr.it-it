---
description: Inviato una volta a una finestra dopo l'immissione del ciclo modale di passaggio o di ridimensionamento.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Messaggio WM_ENTERSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314869"
---
# <a name="wm_entersizemove-message"></a><span data-ttu-id="a7a5b-103">\_Messaggio ENTERSIZEMOVE WM</span><span class="sxs-lookup"><span data-stu-id="a7a5b-103">WM\_ENTERSIZEMOVE message</span></span>

<span data-ttu-id="a7a5b-104">Inviato una volta a una finestra dopo l'immissione del ciclo modale di passaggio o di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a7a5b-104">Sent one time to a window after it enters the moving or sizing modal loop.</span></span> <span data-ttu-id="a7a5b-105">La finestra entra nel ciclo modale di spostamento o di ridimensionamento quando l'utente fa clic sulla barra del titolo della finestra o sul bordo di ridimensionamento oppure quando la finestra passa il messaggio [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e il parametro *wParam* del messaggio specifica il valore **SC \_ Move** o **SC \_ size** .</span><span class="sxs-lookup"><span data-stu-id="a7a5b-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOVE** or **SC\_SIZE** value.</span></span> <span data-ttu-id="a7a5b-106">L'operazione è completa quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce.</span><span class="sxs-lookup"><span data-stu-id="a7a5b-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="a7a5b-107">Il sistema invia il messaggio **WM \_ ENTERSIZEMOVE** indipendentemente dal fatto che il trascinamento delle finestre complete sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="a7a5b-107">The system sends the **WM\_ENTERSIZEMOVE** message regardless of whether the dragging of full windows is enabled.</span></span>

<span data-ttu-id="a7a5b-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a7a5b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a><span data-ttu-id="a7a5b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7a5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7a5b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7a5b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7a5b-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a7a5b-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a7a5b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7a5b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7a5b-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a7a5b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7a5b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7a5b-114">Return value</span></span>

<span data-ttu-id="a7a5b-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7a5b-115">Type: **LRESULT**</span></span>

<span data-ttu-id="a7a5b-116">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a7a5b-116">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7a5b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7a5b-117">Requirements</span></span>



| <span data-ttu-id="a7a5b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7a5b-118">Requirement</span></span> | <span data-ttu-id="a7a5b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a7a5b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a5b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7a5b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a5b-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7a5b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a7a5b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7a5b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a5b-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7a5b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7a5b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7a5b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7a5b-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7a5b-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7a5b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7a5b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7a5b-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a7a5b-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7a5b-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a7a5b-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a7a5b-129">**\_EXITSIZEMOVE WM**</span><span class="sxs-lookup"><span data-stu-id="a7a5b-129">**WM\_EXITSIZEMOVE**</span></span>](wm-exitsizemove.md)
</dt> <dt>

[<span data-ttu-id="a7a5b-130">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="a7a5b-130">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)
</dt> <dt>

<span data-ttu-id="a7a5b-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a7a5b-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7a5b-132">Windows</span><span class="sxs-lookup"><span data-stu-id="a7a5b-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
