---
description: Inviato una volta a una finestra, dopo l'uscita dal ciclo modale di passaggio o di ridimensionamento.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Messaggio WM_EXITSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314866"
---
# <a name="wm_exitsizemove-message"></a><span data-ttu-id="6e0c1-103">\_Messaggio EXITSIZEMOVE WM</span><span class="sxs-lookup"><span data-stu-id="6e0c1-103">WM\_EXITSIZEMOVE message</span></span>

<span data-ttu-id="6e0c1-104">Inviato una volta a una finestra, dopo l'uscita dal ciclo modale di passaggio o di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="6e0c1-104">Sent one time to a window, after it has exited the moving or sizing modal loop.</span></span> <span data-ttu-id="6e0c1-105">La finestra entra nel ciclo modale di movimento o di ridimensionamento quando l'utente fa clic sulla barra del titolo della finestra o sul bordo di ridimensionamento oppure quando la finestra passa il messaggio [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e il parametro *wParam* del messaggio specifica il valore della **\_ dimensione** **SC \_ MOV** e o SC.</span><span class="sxs-lookup"><span data-stu-id="6e0c1-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOV** E or **SC\_SIZE** value.</span></span> <span data-ttu-id="6e0c1-106">L'operazione è completa quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce.</span><span class="sxs-lookup"><span data-stu-id="6e0c1-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="6e0c1-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6e0c1-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a><span data-ttu-id="6e0c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e0c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e0c1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e0c1-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="6e0c1-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e0c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e0c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e0c1-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="6e0c1-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0c1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e0c1-113">Return value</span></span>

<span data-ttu-id="6e0c1-114">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6e0c1-114">Type: **LRESULT**</span></span>

<span data-ttu-id="6e0c1-115">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6e0c1-115">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0c1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e0c1-116">Requirements</span></span>



| <span data-ttu-id="6e0c1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0c1-117">Requirement</span></span> | <span data-ttu-id="6e0c1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6e0c1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0c1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e0c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0c1-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e0c1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e0c1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e0c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0c1-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e0c1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e0c1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e0c1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e0c1-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c1-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e0c1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e0c1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e0c1-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6e0c1-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6e0c1-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6e0c1-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6e0c1-128">**\_ENTERSIZEMOVE WM**</span><span class="sxs-lookup"><span data-stu-id="6e0c1-128">**WM\_ENTERSIZEMOVE**</span></span>](wm-entersizemove.md)
</dt> <dt>

<span data-ttu-id="6e0c1-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6e0c1-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6e0c1-130">Windows</span><span class="sxs-lookup"><span data-stu-id="6e0c1-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
