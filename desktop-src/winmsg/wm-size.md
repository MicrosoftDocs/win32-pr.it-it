---
Description: Inviato a una finestra dopo la modifica delle dimensioni.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Messaggio WM_SIZE (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333633"
---
# <a name="wm_size-message"></a><span data-ttu-id="b07b6-103">\_Messaggio dimensioni WM</span><span class="sxs-lookup"><span data-stu-id="b07b6-103">WM\_SIZE message</span></span>

<span data-ttu-id="b07b6-104">Inviato a una finestra dopo la modifica delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b07b6-104">Sent to a window after its size has changed.</span></span>

<span data-ttu-id="b07b6-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="b07b6-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a><span data-ttu-id="b07b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b07b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b07b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b07b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b07b6-108">Tipo di ridimensionamento richiesto.</span><span class="sxs-lookup"><span data-stu-id="b07b6-108">The type of resizing requested.</span></span> <span data-ttu-id="b07b6-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b07b6-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b07b6-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b07b6-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="b07b6-111">Significato</span><span class="sxs-lookup"><span data-stu-id="b07b6-111">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <span data-ttu-id="b07b6-112"><dt>**Dimensioni \_ MAXHIDE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b07b6-112"><dt>**SIZE\_MAXHIDE**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="b07b6-113">Il messaggio viene inviato a tutte le finestre popup quando un'altra finestra è ingrandita.</span><span class="sxs-lookup"><span data-stu-id="b07b6-113">Message is sent to all pop-up windows when some other window is maximized.</span></span><br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <span data-ttu-id="b07b6-114"><dt>**Dimensioni \_ Ingrandita**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b07b6-114"><dt>**SIZE\_MAXIMIZED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b07b6-115">La finestra è stata ingrandita.</span><span class="sxs-lookup"><span data-stu-id="b07b6-115">The window has been maximized.</span></span><br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <span data-ttu-id="b07b6-116"><dt>**Dimensioni \_ MAXSHOW**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b07b6-116"><dt>**SIZE\_MAXSHOW**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="b07b6-117">Il messaggio viene inviato a tutte le finestre popup quando un'altra finestra è stata ripristinata alle dimensioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b07b6-117">Message is sent to all pop-up windows when some other window has been restored to its former size.</span></span><br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <span data-ttu-id="b07b6-118"><dt>**Dimensioni \_ RIDOTTO a icona**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b07b6-118"><dt>**SIZE\_MINIMIZED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b07b6-119">La finestra è stata ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="b07b6-119">The window has been minimized.</span></span><br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <span data-ttu-id="b07b6-120"><dt>**Dimensioni \_ RIPRISTINAto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b07b6-120"><dt>**SIZE\_RESTORED**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="b07b6-121">La finestra è stata ridimensionata, ma non è stata applicata la **\_ riduzione delle dimensioni** né il valore **\_ ingrandito delle dimensioni** .</span><span class="sxs-lookup"><span data-stu-id="b07b6-121">The window has been resized, but neither the **SIZE\_MINIMIZED** nor **SIZE\_MAXIMIZED** value applies.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b07b6-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b07b6-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b07b6-123">La parola di ordine inferiore di *lParam* specifica la nuova larghezza dell'area client.</span><span class="sxs-lookup"><span data-stu-id="b07b6-123">The low-order word of *lParam* specifies the new width of the client area.</span></span>

<span data-ttu-id="b07b6-124">La parola di ordine superiore di *lParam* specifica la nuova altezza dell'area client.</span><span class="sxs-lookup"><span data-stu-id="b07b6-124">The high-order word of *lParam* specifies the new height of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b07b6-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b07b6-125">Return value</span></span>

<span data-ttu-id="b07b6-126">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b07b6-126">Type: **LRESULT**</span></span>

<span data-ttu-id="b07b6-127">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="b07b6-127">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="b07b6-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="b07b6-128">Example</span></span>

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

<span data-ttu-id="b07b6-129">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="b07b6-129">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="b07b6-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b07b6-130">Remarks</span></span>

<span data-ttu-id="b07b6-131">Se per una finestra figlio viene chiamata la funzione [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) o [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) come risultato del messaggio di **\_ dimensioni WM** , il parametro *bRedraw* o *bRepaint* deve essere diverso da zero per fare in modo che la finestra venga ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="b07b6-131">If the [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) or [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function is called for a child window as a result of the **WM\_SIZE** message, the *bRedraw* or *bRepaint* parameter should be nonzero to cause the window to be repainted.</span></span>

<span data-ttu-id="b07b6-132">Sebbene la larghezza e l'altezza di una finestra siano valori a 32 bit, il parametro *lParam* contiene solo i 16 bit di ogni ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="b07b6-132">Although the width and height of a window are 32-bit values, the *lParam* parameter contains only the low-order 16 bits of each.</span></span>

<span data-ttu-id="b07b6-133">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i messaggi di **\_ dimensioni WM** e di **\_ spostamento WM** quando elabora il messaggio [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="b07b6-133">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="b07b6-134">I messaggi WM **\_ size** e **WM \_ Move** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="b07b6-134">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b07b6-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b07b6-135">Requirements</span></span>



| <span data-ttu-id="b07b6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b07b6-136">Requirement</span></span> | <span data-ttu-id="b07b6-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b07b6-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07b6-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b07b6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b07b6-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b07b6-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b07b6-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b07b6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b07b6-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b07b6-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b07b6-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b07b6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b07b6-143"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b07b6-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b07b6-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b07b6-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="b07b6-145">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b07b6-145">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="b07b6-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b07b6-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b07b6-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b07b6-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b07b6-148">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="b07b6-148">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="b07b6-149">**\_WINDOWPOSCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="b07b6-149">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="b07b6-150">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b07b6-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b07b6-151">Windows</span><span class="sxs-lookup"><span data-stu-id="b07b6-151">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="b07b6-152">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="b07b6-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="b07b6-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="b07b6-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

 
