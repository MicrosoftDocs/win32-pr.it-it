---
Description: Inviato come segnale del termine di una finestra o di un'applicazione.
ms.assetid: 19500baf-e0ad-4dfa-804f-6a6e0652cffb
title: Messaggio WM_CLOSE (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2f1403050cfd3c98ddf90df4399547158a583c50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328992"
---
# <a name="wm_close-message"></a><span data-ttu-id="32cba-103">\_Messaggio di chiusura WM</span><span class="sxs-lookup"><span data-stu-id="32cba-103">WM\_CLOSE message</span></span>

<span data-ttu-id="32cba-104">Inviato come segnale del termine di una finestra o di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32cba-104">Sent as a signal that a window or an application should terminate.</span></span>

<span data-ttu-id="32cba-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="32cba-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CLOSE                        0x0010
```



## <a name="parameters"></a><span data-ttu-id="32cba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32cba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32cba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32cba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32cba-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="32cba-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="32cba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32cba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32cba-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="32cba-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32cba-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32cba-111">Return value</span></span>

<span data-ttu-id="32cba-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="32cba-112">Type: **LRESULT**</span></span>

<span data-ttu-id="32cba-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="32cba-113">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="32cba-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="32cba-114">Example</span></span>

```cpp
LRESULT CALLBACK WindowProc(
    __in HWND hWindow,
    __in UINT uMsg,
    __in WPARAM wParam,
    __in LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CLOSE:
        DestroyWindow(hWindow);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWindow, uMsg, wParam, lParam);
    }

    return 0;
}
```
<span data-ttu-id="32cba-115">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="32cba-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="32cba-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="32cba-116">Remarks</span></span>

<span data-ttu-id="32cba-117">Un'applicazione può richiedere conferma all'utente, prima di eliminare definitivamente una finestra, elaborando il messaggio **WM \_ Close** e chiamando la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) solo se l'utente conferma la scelta.</span><span class="sxs-lookup"><span data-stu-id="32cba-117">An application can prompt the user for confirmation, prior to destroying a window, by processing the **WM\_CLOSE** message and calling the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function only if the user confirms the choice.</span></span>

<span data-ttu-id="32cba-118">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) chiama la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) per eliminare definitivamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="32cba-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function calls the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="32cba-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32cba-119">Requirements</span></span>



| <span data-ttu-id="32cba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="32cba-120">Requirement</span></span> | <span data-ttu-id="32cba-121">Valore</span><span class="sxs-lookup"><span data-stu-id="32cba-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32cba-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32cba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32cba-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32cba-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32cba-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32cba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32cba-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32cba-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32cba-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32cba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="32cba-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32cba-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32cba-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32cba-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="32cba-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="32cba-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32cba-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="32cba-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="32cba-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="32cba-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

<span data-ttu-id="32cba-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="32cba-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32cba-133">Windows</span><span class="sxs-lookup"><span data-stu-id="32cba-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
