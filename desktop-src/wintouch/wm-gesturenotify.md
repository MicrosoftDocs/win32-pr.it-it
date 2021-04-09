---
title: Messaggio WM_GESTURENOTIFY (winuser. h)
description: Offre la possibilità di impostare la configurazione dei movimenti.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY messaggio Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120338"
---
# <a name="wm_gesturenotify-message"></a><span data-ttu-id="c7283-104">\_Messaggio GESTURENOTIFY WM</span><span class="sxs-lookup"><span data-stu-id="c7283-104">WM\_GESTURENOTIFY message</span></span>

<span data-ttu-id="c7283-105">Offre la possibilità di impostare la configurazione dei movimenti.</span><span class="sxs-lookup"><span data-stu-id="c7283-105">Gives you a chance to set the gesture configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7283-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7283-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7283-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7283-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7283-108">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c7283-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c7283-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7283-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7283-110">Puntatore a un [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span><span class="sxs-lookup"><span data-stu-id="c7283-110">A pointer to a [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7283-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7283-111">Return value</span></span>

<span data-ttu-id="c7283-112">Un valore deve essere restituito da [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="c7283-112">A value should be returned from [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7283-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7283-113">Remarks</span></span>

<span data-ttu-id="c7283-114">Quando viene ricevuto il messaggio **WM \_ GESTURENOTIFY** , l'applicazione può usare [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) per specificare i movimenti da ricevere.</span><span class="sxs-lookup"><span data-stu-id="c7283-114">When the **WM\_GESTURENOTIFY** message is received, the application can use [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) to specify the gestures to receive.</span></span> <span data-ttu-id="c7283-115">Questo messaggio deve essere sempre propagato tramite la funzione [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="c7283-115">This message should always be bubbled up using the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="c7283-116">La gestione del messaggio **WM \_ GESTURENOTIFY** modificherà la configurazione dei movimenti per la durata della finestra, non solo per il movimento successivo.</span><span class="sxs-lookup"><span data-stu-id="c7283-116">Handling the **WM\_GESTURENOTIFY** message will change the gesture configuration for the lifetime of the Window, not just for the next gesture.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c7283-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="c7283-117">Examples</span></span>

<span data-ttu-id="c7283-118">Nell'esempio seguente viene illustrato come abilitare tutti i movimenti.</span><span class="sxs-lookup"><span data-stu-id="c7283-118">The following example shows how to enable all gestures.</span></span> <span data-ttu-id="c7283-119">Per altri esempi, vedere [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span><span class="sxs-lookup"><span data-stu-id="c7283-119">For more examples, see [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span></span>


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a><span data-ttu-id="c7283-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7283-120">Requirements</span></span>



| <span data-ttu-id="c7283-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7283-121">Requirement</span></span> | <span data-ttu-id="c7283-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c7283-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7283-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7283-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7283-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c7283-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c7283-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7283-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7283-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7283-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="c7283-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7283-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7283-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7283-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7283-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7283-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7283-130">Notifications</span><span class="sxs-lookup"><span data-stu-id="c7283-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="c7283-131">Guida alla programmazione di movimenti tocco di Windows</span><span class="sxs-lookup"><span data-stu-id="c7283-131">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="c7283-132">**GESTURENOTIFYSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c7283-132">**GESTURENOTIFYSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[<span data-ttu-id="c7283-133">**SetGestureConfig**</span><span class="sxs-lookup"><span data-stu-id="c7283-133">**SetGestureConfig**</span></span>](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

