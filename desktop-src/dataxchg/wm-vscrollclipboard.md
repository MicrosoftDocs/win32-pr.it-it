---
title: Messaggio WM_VSCROLLCLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel \_ formato CF OWNERDISPLAY e si verifica un evento nella barra di scorrimento verticale del visualizzatore degli Appunti.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- Scambio di dati del messaggio WM_VSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477176"
---
# <a name="wm_vscrollclipboard-message"></a><span data-ttu-id="24e88-104">\_Messaggio VSCROLLCLIPBOARD WM</span><span class="sxs-lookup"><span data-stu-id="24e88-104">WM\_VSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="24e88-105">Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e si verifica un evento nella barra di scorrimento verticale del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="24e88-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's vertical scroll bar.</span></span> <span data-ttu-id="24e88-106">Il proprietario deve scorrere l'immagine degli Appunti e aggiornare i valori della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="24e88-106">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a><span data-ttu-id="24e88-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="24e88-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e88-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24e88-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24e88-109">Handle per la finestra del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="24e88-109">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="24e88-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24e88-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24e88-111">La parola di ordine inferiore di *lParam* specifica un evento della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="24e88-111">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="24e88-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="24e88-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="24e88-113">Valore</span><span class="sxs-lookup"><span data-stu-id="24e88-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="24e88-114">Significato</span><span class="sxs-lookup"><span data-stu-id="24e88-114">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="24e88-115"><dt>**SB \_ ULTIMI**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-115"><dt>**SB\_BOTTOM**</dt> <dt>7</dt></span></span> </dl>                      | <span data-ttu-id="24e88-116">Scorrere in basso a destra.</span><span class="sxs-lookup"><span data-stu-id="24e88-116">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="24e88-117"><dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="24e88-118">Fine scorrimento.</span><span class="sxs-lookup"><span data-stu-id="24e88-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="24e88-119"><dt>**SB \_ LINEDOWN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-119"><dt>**SB\_LINEDOWN**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="24e88-120">Scorrere una riga verso il basso.</span><span class="sxs-lookup"><span data-stu-id="24e88-120">Scroll one line down.</span></span><br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="24e88-121"><dt>**SB \_ LINEUP**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-121"><dt>**SB\_LINEUP**</dt> <dt>0</dt></span></span> </dl>                      | <span data-ttu-id="24e88-122">Scorre una riga verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="24e88-122">Scroll one line up.</span></span><br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="24e88-123"><dt>**SB \_ PGGIÙ**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-123"><dt>**SB\_PAGEDOWN**</dt> <dt>3</dt></span></span> </dl>                | <span data-ttu-id="24e88-124">Scorrere una pagina verso il basso.</span><span class="sxs-lookup"><span data-stu-id="24e88-124">Scroll one page down.</span></span><br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="24e88-125"><dt>**SB \_ PAGEUP**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-125"><dt>**SB\_PAGEUP**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="24e88-126">Scorrere una pagina verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="24e88-126">Scroll one page up.</span></span><br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="24e88-127"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-127"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="24e88-128">Scorrere fino alla posizione assoluta.</span><span class="sxs-lookup"><span data-stu-id="24e88-128">Scroll to absolute position.</span></span> <span data-ttu-id="24e88-129">La posizione corrente è specificata dalla parola più avanzata.</span><span class="sxs-lookup"><span data-stu-id="24e88-129">The current position is specified by the high-order word.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="24e88-130"><dt>**SB \_ PRIMI**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-130"><dt>**SB\_TOP**</dt> <dt>6</dt></span></span> </dl>                               | <span data-ttu-id="24e88-131">Scorrere fino alla parte superiore sinistra.</span><span class="sxs-lookup"><span data-stu-id="24e88-131">Scroll to upper left.</span></span><br/>                                                                  |



 

<span data-ttu-id="24e88-132">La parola più significativa di *lParam* specifica la posizione corrente della casella di scorrimento se la parola meno significativa di *lParam* è **SB \_ THUMBPOSITION**. in caso contrario, non viene usata la parola più ordinata di *lParam* .</span><span class="sxs-lookup"><span data-stu-id="24e88-132">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word of *lParam* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e88-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24e88-133">Return value</span></span>

<span data-ttu-id="24e88-134">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="24e88-134">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24e88-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="24e88-135">Remarks</span></span>

<span data-ttu-id="24e88-136">Il proprietario degli Appunti può utilizzare la funzione [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) per scorrere l'immagine nella finestra Visualizzatore Appunti e invalidare l'area appropriata.</span><span class="sxs-lookup"><span data-stu-id="24e88-136">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e88-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24e88-137">Requirements</span></span>



| <span data-ttu-id="24e88-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="24e88-138">Requirement</span></span> | <span data-ttu-id="24e88-139">Valore</span><span class="sxs-lookup"><span data-stu-id="24e88-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24e88-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24e88-140">Minimum supported client</span></span><br/> | <span data-ttu-id="24e88-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24e88-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="24e88-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24e88-142">Minimum supported server</span></span><br/> | <span data-ttu-id="24e88-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24e88-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24e88-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24e88-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="24e88-145"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24e88-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e88-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24e88-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="24e88-147">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="24e88-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="24e88-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24e88-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="24e88-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24e88-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="24e88-150">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="24e88-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24e88-151">Appunti</span><span class="sxs-lookup"><span data-stu-id="24e88-151">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="24e88-152">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="24e88-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="24e88-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="24e88-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

