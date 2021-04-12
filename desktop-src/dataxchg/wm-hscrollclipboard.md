---
title: Messaggio WM_HSCROLLCLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- Scambio di dati del messaggio WM_HSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478304"
---
# <a name="wm_hscrollclipboard-message"></a><span data-ttu-id="3de69-104">\_Messaggio HSCROLLCLIPBOARD WM</span><span class="sxs-lookup"><span data-stu-id="3de69-104">WM\_HSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="3de69-105">Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3de69-105">Sent to the clipboard owner by a clipboard viewer window.</span></span> <span data-ttu-id="3de69-106">Questo errore si verifica quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e si verifica un evento nella barra di scorrimento orizzontale del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3de69-106">This occurs when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's horizontal scroll bar.</span></span> <span data-ttu-id="3de69-107">Il proprietario deve scorrere l'immagine degli Appunti e aggiornare i valori della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3de69-107">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a><span data-ttu-id="3de69-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3de69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3de69-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3de69-110">Handle per la finestra del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3de69-110">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="3de69-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3de69-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3de69-112">La parola di ordine inferiore di *lParam* specifica un evento della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3de69-112">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="3de69-113">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3de69-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="3de69-114">La parola più significativa di *lParam* specifica la posizione corrente della casella di scorrimento se la parola meno significativa di *lParam* è **SB \_ THUMBPOSITION**. in caso contrario, non viene usata la parola più significativa.</span><span class="sxs-lookup"><span data-stu-id="3de69-114">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word is not used.</span></span>



| <span data-ttu-id="3de69-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3de69-115">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="3de69-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3de69-116">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="3de69-117"><dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="3de69-118">Fine scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3de69-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="3de69-119"><dt>**SB \_ SINISTRO**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-119"><dt>**SB\_LEFT**</dt> <dt>6</dt></span></span> </dl>                            | <span data-ttu-id="3de69-120">Scorrere fino alla parte superiore sinistra.</span><span class="sxs-lookup"><span data-stu-id="3de69-120">Scroll to upper left.</span></span><br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="3de69-121"><dt>**SB \_ DIRITTO**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-121"><dt>**SB\_RIGHT**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="3de69-122">Scorrere in basso a destra.</span><span class="sxs-lookup"><span data-stu-id="3de69-122">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="3de69-123"><dt>**SB \_ LINELEFT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-123"><dt>**SB\_LINELEFT**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="3de69-124">Scorre verso sinistra di un'unità.</span><span class="sxs-lookup"><span data-stu-id="3de69-124">Scrolls left by one unit.</span></span><br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="3de69-125"><dt>**SB \_ LINERIGHT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-125"><dt>**SB\_LINERIGHT**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="3de69-126">Scorre verso destra di un'unità.</span><span class="sxs-lookup"><span data-stu-id="3de69-126">Scrolls right by one unit.</span></span><br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="3de69-127"><dt>**SB \_ PAGELEFT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-127"><dt>**SB\_PAGELEFT**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="3de69-128">Scorre verso sinistra in base alla larghezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="3de69-128">Scrolls left by the width of the window.</span></span><br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="3de69-129"><dt>**SB \_ PAGERIGHT**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-129"><dt>**SB\_PAGERIGHT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="3de69-130">Scorre verso destra in base alla larghezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="3de69-130">Scrolls right by the width of the window.</span></span><br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="3de69-131"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-131"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="3de69-132">Scorrere fino alla posizione assoluta.</span><span class="sxs-lookup"><span data-stu-id="3de69-132">Scroll to absolute position.</span></span> <span data-ttu-id="3de69-133">La posizione corrente è specificata dalla parola più avanzata.</span><span class="sxs-lookup"><span data-stu-id="3de69-133">The current position is specified by the high-order word.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de69-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3de69-134">Return value</span></span>

<span data-ttu-id="3de69-135">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="3de69-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de69-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="3de69-136">Remarks</span></span>

<span data-ttu-id="3de69-137">Il proprietario degli Appunti può utilizzare la funzione [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) per scorrere l'immagine nella finestra Visualizzatore Appunti e invalidare l'area appropriata.</span><span class="sxs-lookup"><span data-stu-id="3de69-137">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de69-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3de69-138">Requirements</span></span>



| <span data-ttu-id="3de69-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3de69-139">Requirement</span></span> | <span data-ttu-id="3de69-140">Valore</span><span class="sxs-lookup"><span data-stu-id="3de69-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de69-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3de69-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3de69-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3de69-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3de69-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3de69-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3de69-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3de69-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3de69-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3de69-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de69-146"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3de69-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de69-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3de69-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="3de69-148">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3de69-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="3de69-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3de69-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3de69-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3de69-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3de69-151">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3de69-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3de69-152">Appunti</span><span class="sxs-lookup"><span data-stu-id="3de69-152">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="3de69-153">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="3de69-153">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="3de69-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="3de69-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

